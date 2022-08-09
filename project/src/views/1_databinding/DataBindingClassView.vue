<template>
  <div>
    <div :class="{'text-red': hasError, 'active': isActive}">클래스 바인딩</div>
    <div :class="class2">클래스 바인딩2</div>
  </div>
  <div>
    <input type="radio" name="hi" id="" value="x" v-model="isActive">
    <input type="radio" name="hi" id="" value="x" v-model="hasError">
  </div>
  <div>
    {{ isActive + hasError }}
  </div>
</template>
<script>
export default {
  components: {},
  data () {
    return {
      isActive: false,
      hasError: false,
      class2: ['isActive', 'hasError']
    }
  },
  setup () {},
  created () {},
  mounted () {},
  unmounted () {},
  methods: {}
}
</script>
<style scoped>
.active {
    background-color: greenyellow;
    font-weight: bold;
}

.text-red {
    color: red;
}
</style>
