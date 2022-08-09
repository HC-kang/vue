<template>
  <div>
    <input type="text" name="" id="" v-bind:value="userId" readonly/>
  </div>
  <div>
    <input type="text" name="" id="" :value="userId" readonly/>
  </div>
  <br>
    <img :src="imgSrc" alt="" style="width: 200px; height:auto;">
  <div>
    {{ userId }}
  <input type="search" name="" id="" v-model="txt1" />
  <button :disabled="txt1===''">조회</button>
  </div>
</template>
<script>
export default {
  components: {},
  data () {
    return {
      userId: 'Hello',
      imgSrc: 'https://images.velog.io/images/woals3000/post/18ca184e-63c6-4bba-b282-a1c8db336fe9/vue.png',
      txt1: ''
    }
  },
  setup () {},
  created () {},
  mounted () {},
  unmounted () {},
  methods: {}
}
</script>
