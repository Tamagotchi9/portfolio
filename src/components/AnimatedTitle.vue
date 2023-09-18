<template>
  <transition name="slide-in" appear>
    <h2 class="font-mono font-semibold text-2xl transition-opacity">
      Hello, My name is Dmytro Voloshko! I'm a Ukrainian FrontEnd Developer. You are viewing my
      porfolio.
    </h2>
  </transition>
</template>

<script>
export default {
  name: 'AnimatedTitle',
  data() {
    return {
      animate: false
    }
  },
  mounted() {
    // this.animate = true
  }
}
</script>

<style scoped lang="scss">
.slide-in-enter-active {
  animation: slide-in 0.5s;
}
.slide-in-leave-active {
  animation: slide-in 0.5s reverse;
}
@keyframes slide-in {
  0% {
    transform: translateY(-500px);
    opacity: 0;
  }
  10% {
    transform: translateY(-450px);
    opacity: 0.1;
  }
  20% {
    transform: translateY(-400px);
    opacity: 0.2;
  }
  30% {
    transform: translateY(-350px);
    opacity: 0.3;
  }
  40% {
    transform: translateY(-300px);
    opacity: 0.4;
  }
  50% {
    transform: translateY(-250px);
    opacity: 0.5;
  }
  60% {
    transform: translateY(-200px);
    opacity: 0.6;
  }
  70% {
    transform: translateY(-150px);
    opacity: 0.7;
  }
  80% {
    transform: translateY(-100px);
    opacity: 0.8;
  }
  90% {
    transform: translateY(-50px);
    opacity: 0.9;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}
</style>
