<template>
  <div class="home">
    <FileComponent></FileComponent>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import FileComponent from '@/components/Filecomponent.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    FileComponent
  }
}
</script>
