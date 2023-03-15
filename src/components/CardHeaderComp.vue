<template>
  <div class="card-header">
    <div class="row">
      <div class="col-2 col-sm-1">
        <img
          class="avatar-img"
          :src="header.picture"
          :alt="`${header.name} avatar`"
        />
      </div>
      <div class="col-8 col-sm-9">
        <h4 class="card-header-title m-0">
            <router-link to="/profile">
                {{ header.name }}
            </router-link>
        </h4>
        <small class="text-muted card-header-subTitle">2 min ago</small>
      </div>
      <div class="col-1">
        <button class="btn d-flex align-items-center more-btn">
          <span class="material-icons-outlined">more_horiz</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardHeaderComp",
  props: ["title", "description", "btns", "picture", "header"],
};
</script>

<style scoped>
.more-btn {
  border-radius: 50%;
  padding: 0.5em;
  margin: 0.3em;
}
.avatar-img {
  width: 40px;
  height: 40px;
  object-fit: cover;
  border-radius: 50%;
}
.card-header-title {
  line-height: 0.7;
}
.card-header-subTitle {
  font-size: 0.8em;
}

.card-header {
  background-color: transparent;
  border-bottom: 0;
}
</style>
∫