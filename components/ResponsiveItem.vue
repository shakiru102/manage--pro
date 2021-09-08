<template>
        <v-container fluid class="content_container">
            <v-layout row wrap>
                <v-flex xs12 sm6 >
                    <slot name="left" ></slot>
                </v-flex>
                <v-flex xs12 sm6 >
                    <slot name="right" ></slot>
                </v-flex>
                <v-flex xs12  >
                    <slot name="bottom" ></slot>
                </v-flex>
            </v-layout>
          </v-container>
</template>

<script>
export default {

}
</script>

<style scoped>
.content_container{
    padding: 0px 5em 7em 5em;
}
@media screen and (max-width: 768px) {
.content_container{
    padding: 0px 3em 7em 3em;
}
}
@media screen and (max-width: 600px) {
.content_container{
    padding: 0px 2em 4em 2em;
}
}

</style>