<template>
  <div id="app">
    <router-view></router-view>
    <l_nav></l_nav>
    <div class="ful">
      <top_header></top_header>
<!--      <electrocardiogram></electrocardiogram>  -->
      <div class="inf">
            
        <l_inf></l_inf>
        <hide></hide>
        <r_inf></r_inf>
        <xia></xia>
      </div>
    </div>

<!--    <h1 v-text="title"></h1>
    <input v-model="newItem" v-on:keyup.enter="addNew">
    <ul>
      <li v-text="item.lable" v-for="item in items" v-bind:class="{finished : item.isFinished}" v-on:click="toggleFinish(item)">
      </li>
    </ul>  -->
  </div>
</template>

<script>
import Store from './store.js'
import header from './components/header.vue'

import l_nav from './components/l_nav.vue'
import electrocardiogram from './components/electrocardiogram.vue'
import l_inf from './components/l_information.vue'
import r_inf from './components/r_information.vue'
import hide from './components/hide_button.vue'
import xia from './components/xia.vue'

export default {
  name: 'app',
  data: function () {
//    return{
//      title: 'this is a todo list',
//      items: Store.fetch(),
//      newItem: '' 
//    }
  },
  
  components: {
    top_header: header ,electrocardiogram ,l_nav ,l_inf ,hide ,r_inf ,xia
  },

  watch: {
//    items: {
//      handler: function (items) {
//        Store.save(items)
//      },
//      deep: true
//    }
  },

  methods: {
//    toggleFinish: function(item){
//      item.isFinished = !item.isFinished
//    },
//    addNew: function(){
//      this.items.push({
//        lable: this.newItem,
//        isFinished: false
//      })
//      this.newItem=''
//    }
  }
}
</script>

<style>
.finished{
  text-decoration: underline;
}

.ful{
  width: 1300px;
  height: 1050px;
}

.inf{
  width: 1300px;
  height: 950px;
  position: relative;
}

#app { 
  font-family: 'Avenir', Helvetica, Arial, sans-serif;

} 

</style>
