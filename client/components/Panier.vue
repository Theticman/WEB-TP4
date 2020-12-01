<template>
  <div>
    <h2>Mon Panier</h2>
    <!-- TODO -->
    <article v-for="article in panier.articles" :key="article.id">
      <div>Wesh la street</div>
    </article>
  </div>
</template>

<script>
module.exports = {
  props: {
    articles: { type: Array, default: [] },
    panier: { type: Object }
  },
  data () {
    return {
    }
  },
  async mounted () {
  },
  methods: {
  }
}
</script>

<style scoped>
</style>
