<template>
  <ul class="list-group">
    <li class="list-group-item text-muted">A 10 personas les gusta tu post</li>
    <li class="list-group-item">
      <div class="row">
        <div class="col d-grid">
          <button class="btn d-flex justify-content-center align-items-center gap-2 px-0">
            <span class="material-icons-outlined">thumb_up</span>
            Me gusta
          </button>
        </div>
        <div class="col d-grid">
          <button class="btn d-flex justify-content-center align-items-center gap-2 px-0">
            <span class="material-icons-outlined">chat_bubble_outline</span>
            Comentar
          </button>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
export default {};
</script>

<style scoped>
    .btn:hover {
        color: #5044c9;
    }
</style>
