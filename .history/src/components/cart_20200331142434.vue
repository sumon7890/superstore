<template>
<div id="app">
<ul class="list-group">
      <li class="list-group-item">
        <span class="item-name">Name</span>
        <span class="item-name float-right">Price</span>
      </li>
      <hr/>
      <li class="list-group-item" v-for="(item, index) in items" :key="index">
        <span class="item-name">{{ item.title }}</span>
        <span class="item-name float-right">{{ item.Price }}</span>
      </li>
      <hr/>
      <li class="list-group-item">
        <span class="item-name">Total</span>
        <span class="item-name float-right">{{ totalPrice }}</span>
      </li>
      <hr/>

  </ul>



</div>
</template>

<script>


export default {
props:['items'],
computed:{
//   totalPrice(){
//   var total = 0;
//   var item1;
//   this.items.forEach(item => {
//   item1 = JSON.parse(JSON.stringify(item)),
//   total += parseFloat(item.Price)
//   });
//   return total
// }
// }

// }

totalPrice(){
    var total = 0
    this.items.forEach(item => {
      total += parseFloat(item.Price)
    });
    return total
  }
}
}
</script>

<style>

</style>
