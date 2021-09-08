<template>
  <responsive-item>
            <template v-slot:left>
                <div   class="content_title hidden-xs-only ">
                    Bring everyone together to build better products.
                </div>
                <div class=" hidden-xs-only content_text">
                    Manage makes it simple for software teams to plan dady-to-day tasks while keeping the larger team goals in view
                </div>
                <div class="hidden-xs-only">
                  <Button text="Get Started"  buttonstyle="hsl(12, 88%, 59%)" textstyle="btn_primary"/>
                </div>
                <img class="illustration hidden-sm-and-up  " src="@/assets/images/illustration-intro.svg" alt="">
            </template>

            <template v-slot:right>
              <div class="content_title hidden-sm-and-up ">
                    Bring everyone together to build better products.
                </div>
                <div class=" hidden-sm-and-up content_text">
                    Manage makes it simple for software teams to plan dady-to-day tasks while keeping the larger team goals in view
                </div>
                <div class="hidden-sm-and-up text-center">
                  <Button text="Get Started"  buttonstyle="hsl(12, 88%, 59%)" textstyle="btn_primary"/>
                </div>
              <img class="illustration hidden-xs-only" src="@/assets/images/illustration-intro.svg" alt="">
        </template>
        </responsive-item>
</template>

<script>
export default {

}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Be+Vietnam:ital,wght@0,100;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');

.illustration{
    position: relative;
    z-index: 2;
}
.content_title{
  color: hsl(228, 39%, 23%);
  font-family: Be Vietnam, "sans-serif";
  font-weight: bold;
  font-size: 3em;
  padding-right: 1em;
  margin-top: 1em;
  position: relative;
  z-index: 2;
  animation: contentTitle 0.3s linear;
  transition: all 0.3s ease-in-out;
}

@keyframes contentTitle {
  from{
    transform: translateX(100px);
    opacity: 0;
  }to{
    transform: translateX(0);
    opacity: 1;
  }
  
}

.content_text{
  color: hsl(227, 12%, 61%);
  font-family: Be Vietnam, "sans-serif";
  font-size: 1.1em;
  width: 70%;
  margin: 2em 0px 2em 0px;
  position: relative;
    z-index: 2;
    animation: contentText 0.3s linear;
  transition: all 0.3s ease-in-out;

}
@keyframes contentText {
  from{
    transform: translateY(100px);
    opacity: 0;
  }to{
    transform: translateY(0);
    opacity: 1;
  }
  
}
@media screen and (max-width: 768px) {
  .content_title{
    font-size: 1.7em;
  }
  .illustration{
    height: 300px;
  }
  .content_text{
    width: 90%;
    font-size: 0.8em;
  }
}
@media screen and (max-width: 600px) {
  .content_title{
    font-size: 1.5em;
    text-align: center;
    padding-right: 0px;

  }
  .illustration{
    margin-top: 1em;
  }
  .content_text{
    z-index: 100;
    width: 100%;
    font-size: 0.8em;
    text-align: center;

  }
}

</style>