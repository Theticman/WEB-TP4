<template>
  <div>
    <h2>Mon Panier</h2>
    <!-- TODO -->
    <article v-for="article in panier.articles" :key="article.id">
      <div class="article-img">
        <div :style="{ backgroundImage: 'url(' + articles[article.id-1].image + ')' }">
        </div>
      </div>
      <div class="article-content">
      <div class="article-title">
          <h2>{{ articles[article.id-1].name }} - {{ articles[article.id-1].price }}€ - Quantité : {{article.quantity}}</h2>
          <div>
            <button>Retirer du panier</button>
          </div>
      </div>
      <p>{{ articles[article.id-1].description }}</p>
      </div>
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
article {
  display: flex;
}

.article-img {
  flex: 1;
}

.article-img div {
  width: 100px;
  height: 100px;
  background-size: cover;
}

.article-content {
  flex: 3;
}

.article-title {
  display: flex;
  justify-content: space-between;
}

textarea {
  width: 100%;
}
</style>
