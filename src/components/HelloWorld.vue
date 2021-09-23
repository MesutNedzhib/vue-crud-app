<template>
  <div>
    <h3 class="alert alert-primary"> {{msg}}</h3>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>


<style scoped>

</style>
