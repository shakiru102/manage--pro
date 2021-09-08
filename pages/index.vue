<template>
    <div class="parent">
        <Header />
        <img src="@/assets/images/bg-tablet-pattern.svg" alt="image" class="svg_container" >
        <SectionOne />
        <SectionTwo />
        <SectionThree />
        <FooterSection />
    </div>
</template>

<style scoped>

.parent{
    position: relative;
    min-height: 100vh;
    overflow: hidden;
    
}

.svg_container{
    position: absolute;
    top: -12em;
    right: -15em;
    z-index: 1;
}
@media screen and (max-width: 768px) {
    .svg_container{
        top: -25em;
        right: -30em;
    }
    
}

@media screen and (max-width: 600px) {
    .svg_container{
        top: -2em;
        right: -6em;
        width: 400px
    }
    
}
</style>