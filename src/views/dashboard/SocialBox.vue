<template>
  <div class="social-box" :class="data.name">
    <i class="fa" :class="'fa-' + data.name"></i>
    <div class="chart-wrapper">
      <social-box-chart-example :data="data.lineData" height="90"/>
    </div>
    <ul>
      <li v-for="item in data.keyValues">
        <strong>{{item.value}}</strong>
        <span>{{item.title}}</span>
      </li>
    </ul>
  </div><!--/.social-box-->
</template>

<script>
/*
socialData = [
  {name: 'twitter', lineData:[1,13,9,17,34,41,38],keyValues:[
    {title:'followers',value:'973k'},
    {title:'tweets',value:'1'}
  ]}
]
*/
import SocialBoxChartExample from './SocialBoxChartExample'

export default {
  components: {
    SocialBoxChartExample
  },
  name: 'socialBox',
  props: [
    'data'
  ]
}
</script>
