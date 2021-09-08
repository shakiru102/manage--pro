<template>
    <div class=".parent">
    <img src="@/assets/images/bg-tablet-pattern.svg" alt="image" class="svg_container hidden-xs-only " >
    <responsive-item>
            <template v-slot:bottom >
                <div data-aos="zoom-in"  class="testimonial_title" > What they've said  </div>
                <!-- //carousel -->
                <v-carousel
                    cycle
                    hide-delimiter-background
                    show-arrows-on-hover
                    height="40vh"
                    hide-delimiters
                    progress
                    progress-color="hsl(12, 88%, 59%)"
                    class="hidden-sm-and-up"
                  >
                    <v-carousel-item v-for="( item, index ) in testimonials" :key="index" >
                          <div class="testimonials">
                            <img :src="require(`@/assets/images/${ item.img }`)" alt="">
                            <div class="testimonial_subtitle">{{ item.title }}</div>
                            <div class="testimonial_text">{{ item.description }}</div>
                        </div>
                    </v-carousel-item>
                  </v-carousel>
                <v-container fluid >
                    <v-row>
                    <v-col data-aos="fade-up" class="hidden-sm-and-down" cols="3" v-for="( item, index ) in testimonials" :key="index" >
                        <div class="testimonials">
                            <img :src="require(`@/assets/images/${ item.img }`)" alt="">
                            <div class="testimonial_subtitle">{{ item.title }}</div>
                            <div class="testimonial_text">{{ item.description }}</div>
                        </div>
                    </v-col>
                    <v-col data-aos="fade" cols="12" class="text-center my-10">
                        <Button text="Get Started" buttonstyle="hsl(12, 88%, 59%)" textstyle="btn_primary"/>
                    </v-col>
                    </v-row>
                </v-container>
            </template>
        </responsive-item>
    </div>
</template>

<script>
export default {
    data: () => ({
        testimonials: [
            { img: "avatar-anisha.png", title: "Anisha Li", description: "Manage has supercharged our team's workflow. The ability to maintain visibility on larger milestones at all times keeps everyone motivated. "},
            { img: "avatar-ali.png", title: "Ali Bravo", description: "We have been able to cancel so many other subscription since using Manage. There is no more cross-channel confusion and everyone is much more focused. "},
            { img: "avatar-richard.png", title: "Richard Watts", description: "Manage allows us to provide structure and process, It keep us organized and focused. I can't stop recommending them to everyone i talk to! "},
            { img: "avatar-shanai.png", title: "Shanai Gough", description: "Their softwaare allows us to track. manage and collaborate on our projects from anywhere. It keeps the whole team in-sync without being intrusive."}
        ]
    })
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Be+Vietnam:ital,wght@0,100;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');

*{
  font-family: Be Vietnam, "sans-serif";

}
.parent{
 position: relative;
 overflow-x: hidden;
}
.svg_container{
    position: absolute;
    left: -40%;
    bottom: 35em ;
    z-index: 1;
}
.testimonial_title{
  color: hsl(228, 39%, 23%);
  font-weight: bold;
  font-size: 2.5em;
  text-align: center;
  margin: 0px 0px 3em 0px;
}
.testimonials{
    display: flex;
    flex-direction: column;
    align-items: center;
  background: rgba(128, 128, 128, 0.062);
  padding: 0 1em;
  position: relative;
  z-index: 100;


}
.testimonials img{
  height: 100px;
  width: 100px;
  position: relative;
  top: -3em;
}
.testimonial_subtitle{
  color: hsl(228, 39%, 23%);
  font-weight: bold;
    position: relative;
    bottom: 2em;
}
.testimonial_text{
    text-align: center;
    font-size: 0.7em;
    color: hsl(227, 12%, 61%);
    position: relative;
    bottom: 1.5em;

}
@media screen and (max-width: 768px) {
    .svg_container{
    left: -80%;
    bottom: 42em ; 
    }
    .testimonials{
        top: 3em ;
        padding-bottom: 1em ;
    }
    .testimonial_title{
    font-size: 1.5em;

    }
   
}
@media screen and (max-width:600px){
    .testimonial_title{
    font-size: 1.3em;

    }
}

</style>