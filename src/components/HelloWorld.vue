<template>
<div class="container">
    <v-row justify="center">
      <v-expansion-panels accordion>
        <v-expansion-panel
          v-for="(item,i) in titles"
          :key="i"
        >
          <v-expansion-panel-header>{{ item }}</v-expansion-panel-header>
          <v-expansion-panel-content>
            <ListMath/>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-row>
</div>
</template>

<script>
import ListMath from './ListMath';

export default {
  components: {
    ListMath,
  },
  data() {
    return {
      titles: [
        'Funciones matemáticas y físicas',
      ]
    }
  }
}
</script>
