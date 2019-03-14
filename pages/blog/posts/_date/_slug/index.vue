<template>
  <div>
    <h1>{{ title }}</h1>
    <div class="post-meta">
      <time>
        {{ params.date }}
      </time>
      <div v-html="bodyHtml"/>
    </div>
  </div>
</template>

<script lang="ts">
import {
	Component,
	Vue
} from "nuxt-property-decorator";

import { sourceFileArray } from '~/summary.json';

@Component({
  head() {
    const title = `${this.title} - example.com`;
    const url = `https://example.com/posts/${this.params.date}/${this.params.slug}/`;
    return {
      title: title,
      meta: [
        { hid: 'og:url', property: 'og:url', content: url },
        { hid: 'og:title', property: 'og:title', content: title },
      ],
      link: [{ rel: 'canonical', href: url }],
    };
  }
})
export default class extends Vue {
  validate({ params }) {
    return sourceFileArray.includes(`content/posts/${params.date}-${params.slug}.md`);
  }

  asyncData({ params }) {
    /*
     * TODO: add twitter OGP
     */
    return Object.assign({}, require(`~/content/posts/json/${params.date}-${params.slug}.json`), { params });
  }
}
</script>
