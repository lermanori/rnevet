<template>
    <div> 
        <v-icon :ref="`icon`" x-large dark v-for="index in 10" :key="index" class="ma-5" >spa</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="index in 10" :key="index" class="ma-5" >all_inclusive</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="index in 10" :key="index" class="ma-5" >fitness_center</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="index in 10" :key="index" class="ma-5" >kitchen</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="index in 10" :key="index" class="ma-5" >all_inclusive</v-icon>
        <v-icon :ref="`icon`" x-large dark v-for="index in 10" :key="index" class="ma-5" >spa</v-icon>
    </div>
</template>

<script>
export default {


}
</script>

<style scoped>
div{
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
    transform: translate(150px,150px);
  }
  50% {
    transform: translate(0px,150px);
    transform: rotate(400deg);
  }
  100% {
    transform: translate(150px,0px);
    transform: rotate(800deg);
  }
}
.v-icon {
  position: relative;
  animation-name: move;
  animation-duration: 5s;
  animation-timing-function: ease;
  animation-fill-mode: both;
  animation-direction: alternate;
  animation-iteration-count: infinite;
}
</style>
