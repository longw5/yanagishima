<template>
  <div id="page" :class="{unload}">
    <router-view></router-view>
  </div>
</template>

<script>
import {mapState} from 'vuex'

export default {
  name: 'App',
  computed: {
    ...mapState([
      'unload'
    ])
  }
}
</script>

<style>
.unload {
  display: none;
}

.dropdown-menu.show {
  opacity: 0;
  animation: dropdown-show .15s ease-out forwards;
}

@keyframes dropdown-show {
  100% {
    opacity: 1;
  }
}
</style>
