<template>
  <div class="h-screen bg-gradient-to-r from-cyan-500 to-blue-500 background-animate">
    <NuxtPage />
    <UNotifications />
  </div>
</template>


<style scoped>
  .background-animate {
    background-size: 400%;
    -webkit-animation: AnimationName 3s ease infinite;
    -moz-animation: AnimationName 3s ease infinite;
    animation: AnimationName 3s ease infinite;
  }

  @keyframes AnimationName {
    0%,
    100% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
  }
</style>