<template>
 <div>
   <div class="first_footer">
     <responsive-item>
       <template v-slot:bottom>
        <div class="foot_content">
          <div data-aos="fade-left" class="foot_title"> Simplify how your team works today. </div>
          <div data-aos="fade-up" >
         <Button text="Get Started" buttonstyle="white" textstyle="btn_secondary" />
          </div>
        </div>
       </template>
     </responsive-item>
   </div>
   <div class="second_footer">
     <responsive-item>
       <template v-slot:bottom>
          <v-container class="">
            <v-layout row wrap>
              <v-flex xs12 sm4 class="btn_flex" >
                <img :src="require('@/assets/images/footerlogo.svg')" class="hidden-xs-only" />
                 <v-container class="">
                    <v-row>
                     <v-col cols="8" class="hidden-sm-and-up" >
                        <v-text-field dense  outlined rounded color="hsl(12, 88%, 59%)" background-color="white"  placeholder="Updates in your inbox..." ></v-text-field> 
                      </v-col>
                      <v-col cols="4" class="hidden-sm-and-up">
                    <Button text="Go"  buttonstyle="hsl(12, 88%, 59%)" textstyle="btn_neutral"/>
                  </v-col>
                    </v-row>
                  </v-container>
                
                <div class="group_btn hidden-xs-only">
                   <v-btn color="hsl(227, 12%, 61%)"  v-for="(icon, index) in icons" :key="index" icon dark>
                          <v-icon  dark >{{icon}}</v-icon>
                    </v-btn>
                </div>
              </v-flex>
              <v-flex xs12 sm4 >
                 <v-container class="">
                   <v-row>
                        <v-col cols="6" >
                        <div class="footer_navs" v-for="(item, index) in footernavs" :key="index" >{{ item }}</div>
                        </v-col>
                      <v-col cols="6" >
                      <div class="footer_navs" v-for="(item, index) in contnavs" :key="index" >{{ item }}</div>
                    </v-col>
                   </v-row>
                  </v-container>
              </v-flex>
              <v-flex xs12 sm4 >
                 <v-container class="responsive_padding ">
                    <v-row>
                        <v-col cols="10" class="hidden-xs-only" >
                        <v-text-field dense  outlined rounded color="hsl(12, 88%, 59%)" background-color="white"  placeholder="Updates in your inbox..." ></v-text-field> 
                      </v-col>
                      <v-col cols="2" class="hidden-xs-only" >
                    <Button text="Go"  buttonstyle="hsl(12, 88%, 59%)" textstyle="btn_neutral"/>
                  </v-col>
                   <div class=" hidden-sm-and-up xs_btns ">
                   <v-btn color="hsl(227, 12%, 61%)"  v-for="(icon, index) in icons" :key="index" icon dark>
                          <v-icon  dark >{{icon}}</v-icon>
                    </v-btn>
                </div>
                <img :src="require('@/assets/images/footerlogo.svg')" class="hidden-sm-and-up svg_image " />
                   <v-col cols="12">
                     <div class="copyright">Copyright 2020. All Rights Reserved</div>
                   </v-col>
                    </v-row>
                  </v-container>
              </v-flex>
            </v-layout>
           </v-container>
       </template>
     </responsive-item>
   </div>
 </div>
</template>
 
 <script>
 export default {
   data: () => ({
     icons: ["mdi-facebook", "mdi-youtube", "mdi-twitter", "mdi-pinterest", "mdi-instagram"],
     footernavs: ["Home", "Pricing", "Products", "About Us"],
     contnavs: ["Careers", "community", "Privacy Policy"]
   })
 }
 </script>
<style scoped>
.first_footer{
  background-color:hsl(12, 88%, 59%);
  background-image: url('../assets/images/bg-simplify-section-desktop.svg') ;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 10vh;

}
.foot_content{
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  top: 2.5em;
}
.foot_title{
  color: white;
  font-size: 2em;
  width: 30%;
}
.second_footer{
  min-height: 40vh;
  background-color:hsl(233, 12%, 13%);
  padding-top: 4em;

}
.footer_navs{
  color: hsl(227, 12%, 61%);
  margin-top: 0.3em;
}
.flex.btn_flex{
  position: relative;
}
.group_btn{
  position: absolute;
  width: 100%;
  bottom: 0;
}
.copyright{
  color: hsl(227, 12%, 61%);
  text-align: right;
}
 .container.responsive_padding{
    padding-right: 5em;
  }
@media screen and (max-width: 768px) {
  .foot_title{
    font-size: 1.5em;
    width: 40%;

  }
  .container.responsive_padding{
    padding-right: 3em;
  }
  @media screen and (max-width: 600px) {
  .foot_content{
     flex-direction: column;
     padding: 2em ;
    
  }
  .foot_title{
  color: white;
  font-size: 1.5em;
  width: 100%;
  text-align: center;
  margin-bottom: 1em;
}
    
  }
  .xs_btns{
    display: inline-block;
    margin: 1em auto;
  }
  .svg_image{
    margin: 1em auto;
  }
  .copyright{
    font-size: 0.8em;
    text-align: center;
  }
  .footer_navs{
    font-size: 0.8em;
  }
}
</style>