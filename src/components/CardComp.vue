<template>
  <div class="card">
    <CardHeaderComp v-if="header"  :header="header"/>

    <div class="card-body">
      <h5 v-if="title" class="card-title">{{ title }}</h5>
      <p v-if="description" class="card-text">
       {{ description }}
      </p>
      <img v-if="picture" :src="picture" alt="post img" class="post-img">

      <listGroupComp v-if="likes" />

      <slot name="default"></slot>
      <div class="d-grid gap-2">
        <button 
          v-for="btn in btns" 
          :key="btn.txt" 
          class="btn" 
          :class="btn.class"
        >
          {{ btn.txt }}
        </button>
        <slot name="footer"></slot>
      </div>
    </div>
  </div>
</template>

<script>
import CardHeaderComp from './CardHeaderComp.vue';
import ListGroupComp from './ListGroupComp.vue'

export default {
  components: {
    CardHeaderComp,
    ListGroupComp
  },
  name: 'CardComp',
  props: ['title', 'description', 'btns', 'picture', 'header', 'likes']
};
</script>
<style scoped>
    .card {
        border: none;
        box-shadow: 0 2px 4px rgb(0 0 0 / 10%), 0 8px 16px rgb(0 0 0 / 10%);
    }
    .post-img {
      width: 100%;
    }
</style>
