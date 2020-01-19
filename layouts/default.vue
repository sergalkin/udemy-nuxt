<template>
  <div>
    <TheHeader @sidenavToggle="displaySideNav = !displaySideNav"/>
    <TheSidenav :show="displaySideNav" @close="displaySideNav = false"/>
    <nuxt/>
  </div>
</template>

<script>
  import TheHeader from "@/components/Navigation/TheHeader";
  import TheSidenav from "@/components/Navigation/TheSidenav";

  export default {
    components: {
      TheSidenav, TheHeader
    },
    data() {
      return {
        displaySideNav: false
      }
    }
  }
</script>
<style>
  html {
    font-family: 'Roboto', sans-serif;
  }

  body {
    margin: 0;
  }
</style>
