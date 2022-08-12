<template>
  <login />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

// Components
import Login from './Login.vue'

export default defineComponent({
  name: 'HomeView',

  components: {
    Login
  }
})
</script>
