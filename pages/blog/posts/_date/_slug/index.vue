<template>
  <div>
    <h1>{{ title }}</h1>
    <div class="post-meta">
      <time>{{ params.date }}</time>
      <div v-html="bodyHtml"></div>
    </div>
  </div>
</template>

<script>
import { sourceFileArray } from '~/content/posts/json/summary.json'

export default {
  validate({ params }) {
    return sourceFileArray.includes(
      `./content/posts/${params.date}-${params.slug}.md`
    )
  },
  asyncData({ params }) {
    return Object.assign(
      require(`~/content/posts/json/${params.date}-${params.slug}.json`),
      { params }
    )
  },
  head() {
    const title = `${this.title} - Websitename`
    const url = `/blog/posts/${this.params.date}/${this.params.slug}/`

    return {
      title: title,
      meta: [
        // TODO
      ],
      link: [
        {
          rel: 'canonical',
          href: url
        }
      ]
    }
  }
}
</script>
