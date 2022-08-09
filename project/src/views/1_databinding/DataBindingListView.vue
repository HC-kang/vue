<template>
  <div>
    <select name="" id="">
      <option value=""></option>
      <option value="city.code" :key="city.code" v-for="city in cities">{{ city.title }}</option>
    </select>
  </div>
  <div>
    <Table>
      <thead>
        <tr>
          <th>제품번호</th>
          <th>제품명</th>
          <th>가격</th>
          <th>주문수량</th>
          <th>합계</th>
        </tr>
      </thead>
      <tbody>
        <tr :key="i" v-for="(drink, i) in drinkList">{{ drink.drinkName }}
          <td>{{ drink.drinkId }}</td>
          <td>{{ drink.drinkName }}</td>
          <td>{{ drink.price }}</td>
          <td>
            <input type="number" name="" id="" v-model="drink.qty">
          </td>
          <td>{{ drink.qty * drink.price }}</td>
        </tr>
      </tbody>
    </Table>
  </div>
  <div>hi</div>
</template>
<script>
export default {
  components: {},
  data () {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '부산', code: '051' },
        { title: '제주', code: '064' }
      ],
      drinkList: [
        {
          drinkId: '1',
          drinkName: 'Coke',
          price: 700,
          qty: 1
        },
        {
          drinkId: '2',
          drinkName: 'Orange Juice',
          price: 1200,
          qty: 1
        },
        {
          drinkId: '3',
          drinkName: 'Coffee',
          price: 500,
          qty: 1
        },
        {
          drinkId: '4',
          drinkName: 'Water',
          price: 700,
          qty: 1
        },
        {
          drinkId: '5',
          drinkName: 'Something',
          price: 700,
          qty: 1
        },
        {
          drinkId: '6',
          drinkName: 'Others',
          price: 700,
          qty: 1
        }
      ]
    }
  },
  setup () {},
  created () {},
  mounted () {},
  unmounted () {},
  methods: {}
}
</script>
