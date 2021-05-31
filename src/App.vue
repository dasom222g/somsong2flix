<template>
  <div class="test">
    <router-link to="/" class="test__anchor">Home </router-link>
    <router-link to="/about" class="test__anchor">About</router-link>
  </div>
  <router-view />
</template>

<style lang="scss">
.test {
  display: block;
  &__anchor {
    color: $gold-200;
  }
}
</style>
