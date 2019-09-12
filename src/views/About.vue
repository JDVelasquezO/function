<template>
<div>
  <h1 class="ml-6 mt-3">Álgebra</h1>
  <br>
   <v-card
    max-width="400"
    class="mx-left pa-2 ml-6"
  >
    <v-card-title>Función exponencial</v-card-title>
    <v-card-text>
      <div class="text--primary">
        Producto
        <vue-mathjax class="headline" :formula="formula"></vue-mathjax>
      </div>
    </v-card-text>
    <v-card-actions>
      <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on }">
        <v-btn
          color="red lighten-2"
          dark
          v-on="on"
        >
          Ejemplo
        </v-btn>
      </template>

      <v-card>
        <v-card-title
          class="headline grey lighten-2"
          primary-title
        >
          Producto de potencias de igual base
        </v-card-title>

        <v-card-text>
          <br><div class="text--primary">
            <vue-mathjax class="headline" :formula="productoExponencial"></vue-mathjax>
          </div>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <div class="flex-grow-1"></div>
          <v-btn
            color="primary"
            text
            @click="dialog = false"
          >
            Entiendo, gracias
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
    </v-card-actions>
  </v-card>
</div>
</template>

<script>
import {VueMathjax} from 'vue-mathjax'

export default {
  components: {
    'vue-mathjax': VueMathjax
  },
  name: 'HelloWorld',
  data () {
    return {
      // formula: '$$x = {-b \\pm \\sqrt{b^2-4ac} \\over 2a}.$$',
      dialog: false,
      formula: '$$a^{m}a^{n} = a^{m+n}$$',
      productoExponencial: '$$x^{3}x^{5} = x^{3+5} = x^{8}$$',
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="css" scoped>
  .card1 {
    padding-right: 30px;
  }
</style>
