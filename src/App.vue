<template>
  <v-app>
    <v-app-bar app color="orange">
        <v-toolbar-title class="headline text-uppercase">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <span>MbM &nbsp;</span><v-icon>mdi-music</v-icon>
        <span class="font-weight-light text-center">Music By Mood</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
      </v-btn>
        <v-navigation-drawer
                v-model="drawer"
                absolute
                bottom
                temporary
        >
            <v-list
                    nav
                    dense
            >
                <v-list-item-group
                        v-model="group"
                        active-class="deep-purple--text text--accent-4"
                >
                    <v-list-item>
                        <v-list-item-title>Foo</v-list-item-title>
                    </v-list-item>

                    <v-list-item>
                        <v-list-item-title>Bar</v-list-item-title>
                    </v-list-item>

                    <v-list-item>
                        <v-list-item-title>Fizz</v-list-item-title>
                    </v-list-item>

                    <v-list-item>
                        <v-list-item-title>Buzz</v-list-item-title>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>

    </v-app-bar>

    <v-content>
        <my-comp/>
    </v-content>
      <v-bottom-navigation
              :value="activeBtn"
              color="deep-purple accent-4"
      >
          <v-btn>
              <span>Recents</span>
              <v-icon>mdi-history</v-icon>
          </v-btn>

          <v-btn>
              <span>Favorites</span>
              <v-icon>mdi-heart</v-icon>
          </v-btn>

          <v-btn>
              <span>Nearby</span>
              <v-icon>mdi-map-marker</v-icon>
          </v-btn>
      </v-bottom-navigation>
  </v-app>
</template>

<script>
import MyComp from "./components/myComp";

export default {
  name: 'App',
  components: {
      MyComp,
  },
  data: () => ({
    drawer: false,
    group: false,
    activeBtn: '',
  }),
};
</script>
