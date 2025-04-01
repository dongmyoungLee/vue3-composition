<template>
  <section id="portfolio" class="container">
    <h1>Portfolio</h1>
    <ul class="list row">
      <li v-for="(portFolio, idx) in data" :key="idx + 'portFolio'" class="col-md-4">
        <img :src="portFolio.imgUrl" alt="1">
        <h3>{{ portFolio.title }}</h3>
        <p>{{ portFolio.desc }}</p>
        <router-link class="btn btn-primary" :to="'/detail/' + portFolio.id">상세보기</router-link>
      </li>
    </ul>

  </section>
</template>

<script setup>
  defineProps({
    data: Array,
  })
</script>

<style lang="scss" scoped>
  #portfolio {
    h1 { margin-bottom: 1rem; }
    .list {
      list-style-type: none;
      padding: 0;

      li {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin-bottom: 10vh;
        img {
          width: 100%;
          aspect-ratio: 16 / 9;
          object-fit: cover;
          object-position: top;
        }
        h4 { margin-top: 1rem; }
      }
    }
  }

</style>