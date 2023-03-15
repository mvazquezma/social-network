<template>
  <div class="posts container">
    <img src="../assets/img/mazebook.svg" alt="logo" class="logo">
    <CardComp 
      class="mt-2 mx-auto single-post"
      picture="https://images.pexels.com/photos/2422915/pexels-photo-2422915.jpeg?auto=compress&cs=tinysrgb&w=1600"
      description="Post 1" 
      :header="{
        name: 'Avery Lewis', 
        picture: 'https://randomuser.me/api/portraits/women/31.jpg'
      }"
      :likes="true"
    />

    <CardComp 
      class="mt-2 mx-auto single-post"
      picture="https://images.pexels.com/photos/3635300/pexels-photo-3635300.jpeg?auto=compress&cs=tinysrgb&w=1600"
      description="Post 2" 
      :header="{
        name: 'Jeremy Rivera', 
        picture: 'https://randomuser.me/api/portraits/men/25.jpg'
      }"
      :likes="true"
    />

    <CardComp 
      class="mt-2 mx-auto single-post"
      picture="https://images.pexels.com/photos/3244513/pexels-photo-3244513.jpeg?auto=compress&cs=tinysrgb&w=1600"
      description="Post 3"
      :header="{
        name: 'Anne Freeman', 
        picture: 'https://randomuser.me/api/portraits/women/88.jpg'
      }"
      :likes="true"
    />
  </div>
</template>

<script>
import CardComp from '@/components/CardComp.vue'

export default {
  name: "PostsView",
  components: {
    CardComp,
  }
}
</script>

<style scoped>
.posts {
  min-height: 60vh;
  max-width: 895px;
  margin: auto;
}
.logo {
  max-width: 115px;
  padding: .2rem;
}

.single-post {
  max-width: 550px;;
}
</style>