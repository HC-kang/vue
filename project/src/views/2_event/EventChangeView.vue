<template>
  <div>
    <p>{{ selectedCity }}</p>
    <select name="" id="" @change="changeCity($event)" v-model="selectedCity">
        <option value="">==도시선택==</option>
        <option :value="city.cityCode" :key="i" v-for="(city, i) in cityList">{{ city.title }}</option>
    </select>
    <select name="" id="">
        <option value="">==동선택==</option>
        <option value="" :key="i" v-for="(dong, i) in selectedDongList">{{ dong.dongTitle }}</option>
    </select>
    <select name="" id="">
        <option value="">==동선택==</option>
        <option value="" :key="i" v-for="(dong, i) in dongList.filter(dong=>dong.cityCode===selectedCity)">{{ dong.dongTitle }}</option>
    </select>
  </div>
</template>
<script>
export default {
  components: {},
  data () {
    return {
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: 'Seoul' },
        { cityCode: '051', title: 'Busan' },
        { cityCode: '064', title: 'Jeju' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '서울1동' },
        { cityCode: '02', dongCode: '2', dongTitle: '서울2동' },
        { cityCode: '051', dongCode: '3', dongTitle: '부산1동' },
        { cityCode: '051', dongCode: '4', dongTitle: '부산2동' },
        { cityCode: '064', dongCode: '5', dongTitle: '제주1동' },
        { cityCode: '064', dongCode: '6', dongTitle: '제주2동' }
      ],
      selectedDongList: []
    }
  },
  setup () {},
  created () {},
  mounted () {},
  unmounted () {},
  methods: {
    changeCity(event) {
      console.log(event.target.tagName)
      this.selectedDongList = this.dongList.filter(
        (dong) => dong.cityCode === this.selectedCity
      )
    }
  }
}
</script>
