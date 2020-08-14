<template>
  <nav>
      <v-app-bar app class="indigo">
          <v-app-bar-nav-icon class="white--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
          <v-toolbar-title class="text-uppercase white--text">
              <span class="font-weight-light">Jansen Verhuur</span>
              <span> App</span>
          </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn outlined color="white" class="hidden-sm-and-down"> 
              <span>Uitloggen</span>
              <v-icon right>mdi-exit-to-app</v-icon>           
          </v-btn>
      </v-app-bar>

    <v-navigation-drawer dark app v-model="drawer"  class="indigo" >
         <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
             <span class="font-weight-light">Jansen Verhuur</span>
              <span> App</span>
          </v-list-item-title>
          <v-list-item-subtitle>
            Username
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>
         <v-list dense nav>
        <v-list-item
          v-for="item in links"
          :key="item.title"
          link router :to="item.route"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

       <template v-slot:append >
        <div class="pa-2 hidden-md-and-up">
          <v-btn block>Uitloggen</v-btn>
        </div>
      </template>
    </v-navigation-drawer>

   
  </nav>
</template>

<script>
export default {
    name: "NavBar",
    data(){
        return {
            drawer: false,
            links: [
                {
                    icon:"mdi-view-dashboard",
                    title:"Dashboard",
                    route: "/Dashboard"
                },
                {
                    icon:"mdi-calendar",
                    title:"Verhuur",
                    route:""
                },
                {
                    icon:"mdi-package",
                    title:"Inventaris",
                    route:"/Inventory"
                },
                {
                    icon: "mdi-account-multiple",
                    title: "Werknemers",
                    route:"/Employees"
                }
            ]           
        }
    }

}
</script>

<style>

</style>