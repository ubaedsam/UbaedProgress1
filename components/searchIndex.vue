<template>
    <div
      class="max-w-3xl max-w-5xlmin-h-screen flex justify-center mx-auto my-12"
    >
      <main class="w-full">
        <h1 class="text-2xl font-semibold mb-6">My awesome blog</h1>
        <section>
          <form class="flex flex-col space-y-2 mb-4">
            <label for="search-blogs" class>Search blogs</label>
            <input
              id="search-blogs"
              v-model="query"
              class="px-3 py-2 shadow border border-gray-200"
              type="text"
            />
          </form>
        </section>
        <!-- <section class="space-y-4 divide-y">
          <article v-for="post of posts" :key="post.slug" class="pt-4">
            <h2 class="text-lg mb-2 text-blue-700 hover:text-blue-800">
              <nuxt-link :to="`/blog/${post.slug}`">
                {{ post.title }}
              </nuxt-link>
            </h2>
            <span>
              {{ post.description }}
            </span>
          </article>
        </section> -->
      </main>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        query: '',
        products: [],
      }
    },
    async fetch() {
      if (!this.query) {
        this.products = await this.$content("products").fetch()
        return
      }
      this.products = await this.$content("products").search(this.query).fetch()
    },
    watch: {
      query: '$fetch',
    },
  }
  </script>