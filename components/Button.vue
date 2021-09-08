<template>
    <v-btn large  rounded depressed :color="buttonstyle"  :class="textstyle">{{ text }}</v-btn>
</template>
<script>
export default {
    props: ['buttonstyle', 'textstyle', "text"]
}
</script>
<style scoped>
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