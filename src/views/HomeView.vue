<template>
  <div class="home container">
    <div class="row">
      <div class="col-lg-6">
        <div class="img-cont">
          <img alt="Mazebook logo" src="../assets/img/mazebook.svg" />
          <h2 class="text-center text-lg-start mt-3">
            Conéctate con amigos y el resto del undo usando Mazebook
          </h2>
        </div>
      </div>
      <div class="col-lg-6">
        <card-comp :btns="btnArray" class="mx-auto card-comp">
          <form>
            <div class="mb-3 mt-2">
              <input
                type="email"
                class="form-control"
                placeholder="Escribe tu email"
              />
            </div>
            <div class="mb-3 mt-2">
              <input
                type="password"
                class="form-control"
                placeholder="Escribe tu contraseña"
              />
            </div>
          </form>
        </card-comp>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import CardComp from "../components/CardComp.vue";

export default {
  name: "HomeView",
  components: {
    CardComp,
  },
  data() {
    return {
      btnArray: [
        {
          txt: 'Login',
          class: 'btn-primary',
        },
        {
          txt: 'Remove',
          class: 'btn-danger',
        }
      ]
    }
  }
};
</script>

<style scoped>
.home {
  max-width: 895px;
  margin: auto;
}
.img-cont {
  display: flex;
  flex-direction: column;
}
img {
  max-width: 315px;
  margin: 1em auto 0 auto;
}
@media (min-width: 992px) {
  .home {
    margin: 4em auto;
  }
  img {
    margin: 5.6em 0 0;
  }

  h2 {
    text-align: left;
  }
}
.card-comp {
  max-width: 398px;
  margin-top: 2.6em;
}
</style>
