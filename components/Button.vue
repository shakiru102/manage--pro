<template>
    <v-btn large  rounded depressed :color="buttonstyle"  :class="textstyle">{{ text }}</v-btn>
</template>
<script>
export default {
    props: ['buttonstyle', 'textstyle', "text"]
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Be+Vietnam:ital,wght@0,100;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');

.btn_primary{
    font-family: Be Vietnam, "sans-serif";
    text-transform: capitalize;
    box-shadow: 0px 5px 10px hsla(12, 88%, 59%, 0.623) ;
    z-index: 1000;
   color: white;
}
.btn_neutral{
    font-family: Be Vietnam, "sans-serif";
    text-transform: capitalize;
    z-index: 1000;
   color: white;
}
.btn_secondary{
    font-family: Be Vietnam, "sans-serif";
    text-transform: capitalize;
    box-shadow: 0px 5px 10px hsla(12, 88%, 59%, 0.623) ;
    z-index: 1000;
   color: hsl(12, 88%, 59%);
}

</style>