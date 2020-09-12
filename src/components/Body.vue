<template>
    <v-container>
    <v-row dense>       
        <v-col
          v-for="(category, i) in categories"
          :key="i"
          cols="3"
        >
         <v-hover v-slot:default="{ hover }">
          <v-card            
            dark
            style="max-width:300px;"
            
          >
          <v-img 
          :src="category.Bannersrc"
          >
          <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out amber darken-2 v-card--reveal display-1 white--text"
            style="height: 100%;"
             v-text="category.name"
          >
            
          </div>
        </v-expand-transition>
          
                        

    
            </v-img>
          </v-card>
         </v-hover>
          
        </v-col>
      </v-row>
      <User />
    </v-container> 
    
</template>



<script>
export default {
    data: () => {
         return {
      current: {},
      index: 0,      
      categories: [
        {
               
          Bannersrc: require('../assets/cat/wicca.jpg'),
          name: "Wicca/Pagan"
        },       
                  
        {
               
          Bannersrc: require('../assets/cat/candumb.jpg'),
          name: "Candomblé/Umbanda"
        },       
        {
               
          Bannersrc: require('../assets/cat/herm.jpg'),
          name: "Hermetismo"
        },       
                  
      ],
     
    }    
    },
    components: {
      //
  },
    
}
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
</style>

