<template>
  <v-card
    class="mx-auto"
    width="1300"
  >
    <v-list>
      <v-list-item>
        <v-list-item-icon>
          <v-icon>mdi-home</v-icon>
        </v-list-item-icon>

        <v-list-item-title>Funciones</v-list-item-title>
      </v-list-item>

      <v-list-group
        value="true"
      >
        <template v-slot:activator>
          <v-list-item-title>Matemáticas</v-list-item-title>
        </template>

        <v-list-group
          no-action
          sub-group
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title>Álgebra</v-list-item-title>
            </v-list-item-content>
          </template>

          <v-list-item
            v-for="(admin, i) in admins"
            :key="i"
            link
            to="/about"
          >
            <v-list-item-title v-text="admin[0]"></v-list-item-title>
            <v-list-item-icon>
              <v-icon v-text="admin[1]"></v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list-group>

        <v-list-group
          sub-group
          no-action
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title>Geometría</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item
            v-for="(crud, i) in cruds"
            :key="i"
          >
            <v-list-item-title v-text="crud[0]"></v-list-item-title>
            <v-list-item-action>
              <v-icon v-text="crud[1]"></v-icon>
            </v-list-item-action>
          </v-list-item>
        </v-list-group>
      </v-list-group>
    </v-list>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      admins: [
        ['Propiedades de los exponentes'],
        ['Propiedades de los radicales'],
      ],
      cruds: [
        ['Ángulos de un polígono'],
        ['Área y perímetro de cuadriláteros'],
        ['Área y perímetro de triángulos'],
        ['Área y perímetro del círculo'],
      ],
    }),
  }
</script>
