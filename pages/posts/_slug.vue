<template>
  <div>
    <div v-if="$fetchState.pending">
      <!-- por animação de loading -->
    </div>
    <div
      v-else
      class="relative py-16 bg-white dark:bg-indigo-400 overflow-hidden"
    >
      <div class="relative px-4 sm:px-6 lg:px-8">
        <div class="text-lg max-w-prose mx-auto mb-6">
          <h1
            class="
              mt-2
              mb-4
              text-3xl text-center
              leading-8
              font-extrabold
              tracking-tight
              text-gray-900
              sm:text-4xl sm:leading-10
            "
          >
            {{ post[0].attributes.title }}
          </h1>
        </div>
        <div
          v-if="post[0].attributes.body"
          class="prose prose-lg text-justify mx-auto px-5 px-md-50 max-w-4xl"
          v-html="$md.render(post[0].attributes.body)"
        ></div>
        <!-- <div class="prose prose-lg mx-auto mt-4">
          <Date v-if="post.publishedAt" :date="post.publishedAt" />
        </div> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  scrollToTop: true,
  data() {
    return {
      post: [],
    }
  },
  async fetch() {
    const posts = await this.$axios.$get(
      '/api/posts?slug=' + this.$route.params.slug
    )
    this.post = posts.data.filter(
      (p) => p.attributes.slug == this.$route.params.slug
    )
  },

  fetchOnServer: true,
}
</script>
