<template>
  <div class="container p-2 text-center">
    <img
      v-lazy-load
      class="logo"
      data-src="https://www.asiatica-viajes.com/1_2020/assets/images/logo.jpg"
      alt="#"
    />
  </div>
</template>
<style lang="scss">
.logo {
  width: 160px;
  @include media-breakpoint-up(lg) {
    width: 200px;
  }
}
</style>
