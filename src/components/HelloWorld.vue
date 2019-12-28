<template>
  <v-container>
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <v-list dense>
        <v-list-item @click="">
          <v-list-item-action>
            <v-icon>mdi-watch</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="">
          <v-list-item-action>
            <!-- <v-icon>contact_mail</v-icon> -->
            <v-icon>mdi-anchor</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Contact</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      color="indigo"
      dark
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>柯哀王道</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-title>{{ msg }}</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-row align="center" style="max-width: 650px">
        <v-text-field :append-icon-cb="() => {}" placeholder="Search..." single-line append-icon="mdi-watch" color="white"
          hide-details />
      </v-row>
    </v-app-bar>

    <v-content>
      <v-container
        fluid
        fill-height
      >
        <v-layout
          align-center
          justify-center
        >
        <img alt="logo" src="../assets/ka.jpg">
        <!-- <Login/> -->

        </v-layout>
      </v-container>
    </v-content>
    <v-footer
      color="blue-grey lighten-2"
      app
    >
      <span class="white--text">&copy; 2019</span>
    </v-footer>
  </v-container>
</template>

<script>
import Login from './login.vue'

export default {
  name: 'HelloWorld',
  components: {
    Login
  },

  data: () => ({
    drawer: null,
    msg: ''

  }),
  created () {
    this.sayHello()
  },
  methods: {
    sayHello () {
      let date = 'today is a '
      console.log(date)
      this.msg = date + 'buautiful ' + 'day'
    }
  }
}
</script>
