<template>
    <div>
         <v-app-bar height="130px"  class="app_bar" color="transparent" flat >
              <v-toolbar-title>
                <v-img :src="require('@/assets/images/logo.svg')"></v-img>
              </v-toolbar-title>
              <v-spacer></v-spacer>
                     <span v-for="( nav, index ) in navs" :key="index"  class="nav hidden-sm-and-down ">{{ nav.name }}</span>
              <v-spacer></v-spacer>
              <div class="hidden-sm-and-down">
              <Button text="Get Started" buttonstyle="hsl(12, 88%, 59%)" textstyle="btn_primary"/>
              </div>
              <v-app-bar-nav-icon @click="drawer=!drawer" class="hidden-md-and-up "></v-app-bar-nav-icon>
            </v-app-bar>

            <v-navigation-drawer right stateless  app v-model="drawer">
               <v-container class="text-right">
                  <v-row>
                    <v-col>
                      <v-btn @click="drawer=!drawer"  icon color="error" >
                        <v-icon>mdi-close</v-icon>
                      </v-btn>
                    </v-col>
                  </v-row>
                </v-container>
              <v-list>
                <v-list-item :data-aos-delay="nav.time" data-aos="fade-up"  v-for="( nav, index ) in navs" :key="index" >
                  <v-list-item-subtitle>
                        <div   class="text-center text-capitalize mobile_nav">
                        {{ nav.name }}
                        </div>
                  </v-list-item-subtitle>
                </v-list-item>
              </v-list>
            
            </v-navigation-drawer>
    </div>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
    navs: [{ time:0 , name:'pricing'},{ time:300 ,  name:'product'}, { time:350 , name:'about us'}, { time:400 , name:'careers'}, { time:450 , name:'community'}]
  })
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Be+Vietnam:ital,wght@0,100;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
.nav{
  text-transform: capitalize;
  font-family: Be Vietnam, "sans-serif";
  font-size: 0.9em;
  margin-right: 2em;
  color: hsl(228, 39%, 23%);
  font-weight: 600;
  transition: color 0.3s ease-in-out;
  cursor: pointer;
}
.nav:hover{
    color: hsla(228, 39%, 23%, 0.555);
}

.app_bar.v-toolbar{
  z-index: 1000;
  padding:  0px 5em  0px 5em;
}

@media screen and (max-width: 768px) {
.app_bar.v-toolbar{
  z-index: 1000;
  padding:  0px 3em  0px 3em;
}
}
@media screen and (max-width: 600px) {
.app_bar.v-toolbar{
  z-index: 2;
  padding:  0px 0em  0px 0em;
}

.mobile_nav{
  color: hsl(228, 39%, 23%);

}
}
</style>