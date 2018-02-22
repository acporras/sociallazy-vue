<template>
  <b-container>
    <b-navbar toggleable="md" type="dark" variant="info">
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar-brand href="#" class="blessed"><h1>Sociallazy</h1></b-navbar-brand>
      <b-collapse is-nav id="nav_collapse">
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form v-on:submit.prevent="onSubmit">
            <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Buscar en Sociallazy..."/>
            <b-button size="sm" class="my-2 my-sm-0" type="submit"><icon name="search"></icon></b-button>
          </b-nav-form>
          <b-nav-item href="#">Iniciar Sesión</b-nav-item>
          <b-nav-item-dropdown text="Lenguaje" right>
            <b-dropdown-item v-for="language in languages" :data="language" :key="language.code">
              {{ language.code }}
            </b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <br/>
    <div>
      <h3 class="text-center white">Cuando lo que necesitas esta en tus manos</h3>
      <h5 class="text-center white">Una red social para todos</h5>
    </div>
    <br/>
    <div class="text-center">
      <b-button class="text-center" variant="secondary">Empezar Ahora!</b-button>
    </div>
    <div>
      <br/>
      <b-row>
        <b-col>
          <b-card title="Arte"
                  img-src="../assets/img/IMG_20180222_130000.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  style="max-width: 20rem;"
                  class="mb-2">
            <p class="card-text">
              Some quick example text to build on the card title and make up the bulk of the card's content.
            </p>
            <b-button href="#" variant="primary">Go somewhere</b-button>
          </b-card>
        </b-col>
        <b-col>
          <b-card title="Diversión"
                  img-src="../assets/img/IMG_20180222_130023.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  style="max-width: 20rem;"
                  class="mb-2">
            <p class="card-text">
              Some quick example text to build on the card title and make up the bulk of the card's content.
            </p>
            <b-button href="#" variant="primary">Go somewhere</b-button>
          </b-card>
        </b-col>
        <b-col>
          <b-card title="Ocio"
                  img-src="../assets/img/IMG_20180222_130108.png"
                  img-alt="Image"
                  img-top
                  tag="article"
                  style="max-width: 20rem;"
                  class="mb-2">
            <p class="card-text">
              Some quick example text to build on the card title and make up the bulk of the card's content.
            </p>
            <b-button href="#" variant="primary">Go somewhere</b-button>
          </b-card>
        </b-col>
      </b-row>
    </div>
  </b-container>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      languages: [
        { code: 'ES' },
        { code: 'EN' }
      ]
    }
  },
  methods: {
    onSubmit: function () {
      console.log('search')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@font-face {
  font-family: 'Blessed';
  src: url('../assets/fonts/Blessed.ttf');
}
.bg-info{
  background-color: #17a2b800 !important;
}
.blessed{
  font-family: 'Blessed'
}
.white{
  color: #FFFFFF;
}
</style>
