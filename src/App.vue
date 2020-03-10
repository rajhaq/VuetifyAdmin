<template>
  <v-app>
    <Header :items="items" @send="recV"></Header>
       
        <v-content>
      <v-container
        class="fill-height"
        fluid
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col class="text-center">
    <v-card
    class="mx-auto"
    max-width="344"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <div class="overline mb-4">OVERLINE</div>
        <v-list-item-title class="headline mb-1">{{writer}}</v-list-item-title>
        <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      ></v-list-item-avatar>
    </v-list-item>

    <v-card-actions>
      <v-btn text>Button</v-btn>
      <v-btn text>Button</v-btn>
    </v-card-actions>
  </v-card>
          </v-col>
        </v-row>
      </v-container>
        </v-content>

  </v-app>
</template>

<script>
import Header from "./components/Header"

export default {
  name: 'App',

  components: {
    Header
  },

  data: () => ({
    drawer:false,
    writer:"Not clicked",
    items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'About', icon: 'mdi-help-box' },
        ],
        right: null,
    //
  }),
  methods:{
    recV(data)
    {
      this.writer=data;


    }
  }
};
</script>
