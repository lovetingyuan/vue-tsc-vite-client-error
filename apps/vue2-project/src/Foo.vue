<template>
<div>this is foo, under {{dev ? 'dev' :"prod"}} mode</div>
</template>

<script lang="ts">
import  Vue from 'vue'

export default Vue.extend({
  name: 'Foo',
  data() {
    const dev = import.meta.env.DEV
    return {
      message: 'Hello Vue!',
      dev
    }
  }
})

</script>
