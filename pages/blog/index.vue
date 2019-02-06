<template>
  <div>
    <div 
      v-for="(post, index) in posts"
      :key="index"
      class="uk-card uk-card-default uk-grid-collapse uk-child-width-1-2@s uk-margin"
      uk-grid
    >
      <div>
        <div class="uk-card-body">
          <h3 class="uk-card-title">
            <n-link :to="getUrl(post)">
              {{ post.title }}
            </n-link>
          </h3>
          <p class="uk-article-meta">
            Posted at: {{ getDate(post.created_at) }}
          </p>
          <p>
            {{ post.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { fileMap } from '~/content/posts/json/summary.json'

export default {
  asyncData({ params }) {
    return {
      posts: fileMap
    }
  },
  methods: {
    getDate(date) {
      const dt = new Date(date)
      const y = dt.getFullYear()
      const m = ('00' + (dt.getMonth() + 1)).slice(-2)
      const d = ('00' + dt.getDate()).slice(-2)

      return y + '-' + m + '-' + d
    },

    getUrl(post) {
      const date = this.getDate(post.created_at)
      return `/blog/posts/${date}/${post.slug}`
    }
  }
}
</script>
