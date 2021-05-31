<template>
<div>
  <Gsap/>
</div>


</template>

<script>
import Gsap from './components/Gsap'
export default {
  name: 'App',
  components: {
    Gsap
  }
}
</script>

<style>
#app{
  width:700px;
  height:700px;
  background-color: blue;
}
</style>
