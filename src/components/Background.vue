<template>
    <div> 
        <v-icon :ref="`icon`" x-large dark v-for="i1 in number" :key="i1" class="ma-5" >spa</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="i2 in number" :key="i2" class="ma-5" >all_inclusive</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="i3 in number" :key="i3" class="ma-5" >fitness_center</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="i4 in number" :key="i4" class="ma-5" >kitchen</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="i5 in number" :key="i5" class="ma-5" >all_inclusive</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="i6 in number" :key="i6" class="ma-5" >spa</v-icon>
    </div>
</template>

<script>
export default {
computed:{
    number:function(){

        let result = this.$vuetify.breakpoint.xsOnly ? 2 : 10
        console.log(result)
        
        return result;
    }
}

}
</script>

<style scoped>
div{
    margin-top: 5%;
    height: 100%;
    width: 100%;
    position: fixed;
    top: 0;
    left:0;
    background-color: transparent;
    z-index: 0;
}
@keyframes move {
  0% {
    transform: translate(0px,0px);
    transform: rotate(100deg);
  }
  25% {
  }
  50% {
    transform: rotate(400deg);
  }
  75% {
    transform: rotate(600deg);
  }
  100% {
    transform: rotate(800deg);
  }
}
.v-icon {
  position: relative;
  animation-name: move;
  animation-duration: 10s;
  animation-timing-function: ease-in-out;
  animation-fill-mode: both;
  animation-direction: alternate;
  animation-iteration-count: infinite;
}
</style>
