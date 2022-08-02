<template>
  <div>
    <h1 class='text-red'>{{ userName }}</h1>
    <h1 class='text-red'>{{ message }}</h1>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      userName: 'Jone Doe',
      message: 'Hello~~',
      arr: [],
      obj: {}
    }
  }
}
</script>

<style scoped>
.text-red {
  color: red;
}
</style>
