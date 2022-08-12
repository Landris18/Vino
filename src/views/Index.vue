<template>
  <login />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

// Components
import Login from './Login.vue'

export default defineComponent({
  name: 'Index',

  components: {
    Login
  }
})
</script>
