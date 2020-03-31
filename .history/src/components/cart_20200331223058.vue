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
        <span class="item-name float-right">{{ item.Price }}</span><button v-for="removeItem" >Removed</button>
      </li>
      <hr/>
      <li class="list-group-item">
        <span class="item-name">Total</span>
        <span class="item-name float-right">${{ totalPrice }}</span>
      </li>
      <hr/>

  </ul>



</div>
</template>

<script>


export default {
props:['items'],
computed:{
totalPrice() {
      var total = 0;
      var singelPrice;
      var singelPrice1;
      var mainPrice;
      this.items.forEach(item => {
          singelPrice = item.Price;
          if(isNaN(singelPrice)){
            singelPrice1 = singelPrice.split("$");
              mainPrice = singelPrice1[1];
              console.log(mainPrice);
          }else{
              mainPrice = singelPrice;
          }
          total += parseFloat(mainPrice);
      });
      return total;
    }

},
methods:{

}
}
// totalPrice(){
//     var total = 0
//     this.items.forEach(item => {
//       total += parseFloat(item.Price)
//     });
//     return total
//   }

</script>

<style>

</style>
