<template>
  <div>
    <div>
      <h1 class="text-h4 text-center">Dashboard</h1>
      <p class="text-subtitle-1 text-center">Hallo Username!</p>
    </div>

    <v-container>
        <v-layout row wrap>
            <v-flex xs12 sm6 md4 lg3 v-for="item in cards" :key="item.id">
                <v-card  class="text-center ma-3 rounded-br-xl">
                    <div>
                        <v-icon>{{item.icon}}</v-icon>
                    <v-card-title>
                        {{item.title}}
                    </v-card-title>
                    <v-card-text>
                        
                        <div class="grey--text">{{item.data}}</div>
                    </v-card-text>
                    </div>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>

  </div>
</template>

<script>
export default {
    data(){
        return {
            cards:[
                {id: 0,icon:"mdi-wrench", title:"Manco producten", data:0},
                {id: 1,icon:"mdi-briefcase", title:"Vandaag geretourneerd", data:0},
                {id: 2,icon:"mdi-store", title:"Vandaag opgehaald", data:0},
                {id: 3,icon:"mdi-alert-circle", title:"Verhuur conflicten", data:0}
            ]            
        }
    }
};
</script>

<style>
</style>