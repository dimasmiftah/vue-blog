<template>
  <div>
    <add-blog></add-blog>
  </div>
</template>

<script>
import addBlog from './components/addBlog.vue'
export default {
  components: {
    'add-blog' : addBlog,
  },
  data () {
    return {
     
    }
  }
}
</script>

<style>
body{
  margin: 0;
  font-family: 'Open Sans', sans-serif;
}
</style>
