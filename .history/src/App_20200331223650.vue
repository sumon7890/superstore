<template>
<div id="app">

<navber></navber>

<div class="container">
<div class="row">
  <div class="col-md-9">
 <inventory @newItemAdded="addItem" :items="items"></inventory>


</div>

  <div class="col-md-3">
    <cart :items="cart" ></cart>
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
cart:[{
  id:1,
  title:'',
  Price:,
  photo:"http://dummyimage.com/250x250.png/cc0000/ffffff"

}]
  }

},
mounted(){
this.items = data;

},
methods:{
  addItem(item){
    this.cart.push(item)
  }
}
}
</script>

<style>
.container{
  padding: 10px;
}
</style>

