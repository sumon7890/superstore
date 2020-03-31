<template>
<div id="app">

<navber @surach="surch"></navber>

<div class="container">
<div class="row">
  <div class="col-md-9">
 <inventory @newItemAdded="addItem" :items="items"></inventory>


</div>

  <div class="col-md-3">
    <cart @removedItem="removeItem" :items="cart" ></cart>
  </div>
</div>
</div>
</div>
</template>

<script>

import navber from './components/navber'
import inventory from './components/inventory'
import cart from './components/cart'
import data from './router/data'

export default {
components:{
  navber,
  inventory,
  cart
},
data(){
  return{
items:[],
cart:[]
  }

},
mounted(){
this.items = data;

},
methods:{
  surach(keyword){
    this.items.data.filter(item => {
     return item.title.toLowerCase().indexOf(keyword.toLowerCase()) !== -1
    })
  },
  addItem(item){
    this.cart.push(item)
  },
  removeItem(index){
    this.cart.splice(index, 1)
  }
}
}
</script>

<style>
.container{
  padding: 10px;
}
</style>

