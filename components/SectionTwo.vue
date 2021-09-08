<template>
  <responsive-item>
  <template v-slot:left>
          <div data-aos="fade-up"  class="content_title">
              What's different about Manage?
          </div>
          <div data-aos="fade-up"  class="content_text">
              Manage provides all the functionality your team needs. without the complexity. Our software is tailor-made for modern digital product teams.
          </div>
      </template>

      <template v-slot:right>
            <v-container fluid  class="">
              <v-row data-aos="fade-left"  v-for=" item in lists " class="hidden-xs-only"  :key="item.id">
                <v-col cols="2"  >
                    <span class="num">{{ item.id }}</span>
                </v-col>
                <v-col cols="10">
                    <div class="list_title"> <span class="num hidden-sm-and-up ">{{ item.id }}</span> {{ item.title }}</div>
                    <div class="list_text">{{ item.text }}</div>
                </v-col>
              </v-row>
              <v-row v-for=" item in lists " class="hidden-sm-and-up"  :key="item.id">
                <v-col cols="12">
                    <div data-aos="fade-left" class="list_title"> <span class="num mr-1">{{ item.id }}</span> {{ item.title }}</div>
                    <div data-aos="fade-up"  class="list_text">{{ item.text }}</div>
                </v-col>
              </v-row>
            </v-container>
  </template>
</responsive-item>
</template>

<script>
export default {
  data: () => ({
      lists: [
          {id: "01", title: "Track company-wide progress", text: "See how your day-to-day tasks fit into the wider vision. Go from tracking progress at the milestone level all the way done to the smallest of details. Never lose sight of the bigger picture again."},
          {id: "02", title: "Advanced built-in reports", text: "Set internal delivery estimates and track progress toward company goals. Our customisable dashboard helps you build out the reports you need to keep key stakeholders informed."},
          {id: "03", title: "Everything you need in one place", text: "Stop jumping from one service to another to communicate. Store files, track tasks and share documents. Manage offers an all-in-one team productivity solution."}
      ]
  })    
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Be+Vietnam:ital,wght@0,100;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');

*{
  font-family: Be Vietnam, "sans-serif";

}
.content_title{
  color: hsl(228, 39%, 23%);
  font-weight: bold;
  font-size: 2.5em;
  padding-right: 1em;
  position: relative;
  z-index: 100;
  
}

.content_text{
  color: hsl(227, 12%, 61%);
  font-family: Be Vietnam, "sans-serif";
  /* font-size: 1em; */
  width: 70%;
  margin: 2em 0px 0px 0px;
  position: relative;
  z-index: 100;
}


.num{
    background-color: hsl(12, 88%, 59%);
    color: white;
    font-weight: bold;
    padding: 0.5em 1.5em  ;
    border-radius: 20px;
    position: relative;
    top: 0.5em;
    right: 0.5em;
}
.list_title{
    color: hsl(228, 39%, 23%);
    font-weight: bold;
    font-size: 1.2em;
    margin: 0px 0px 1em 0px;
}
.list_text{
  color: hsl(227, 12%, 61%);
  font-family: Be Vietnam, "sans-serif";
 
}
@media screen and (max-width: 768px) {
  .content_title{
    font-size: 1.5em;
  }
  .content_text{
    font-size: 0.8em;
  }
  .num{
    font-size: 0.8em;
  }
  .list_title{
    font-size: 1em;
    
  }
  .list_text{
    font-size: 0.8em;
  }
}
@media screen and (max-width: 600px) {
  .content_title{
    text-align: center;
    font-size: 1.3em;

  }
  .content_text{
    text-align: center;
    width: 100%;
    font-size: 0.7em;
  }
  .num{
    font-size: inherit;
    top: 0;
    right: 0;
    padding: 0em 1em  ;

  }
  .list_title{
    font-size: 0.9em;
     margin: 0px 0px 1em 0px;
     border-radius: 20px 0px 0px 20px;
     background-color: hsla(12, 88%, 59%, 0.364);
  }
  .list_text{
    font-size: 0.7em;
  }
}
</style>