<template>
<div id="app">
    <div class="row">
    <div v-for="(item, index) in items" :key="index" class="card" style="width: 14rem;">
          <img :src="item.photo" class="card-img-top" alt="Card Img">
        <div class="card-body">
          <h5 class="card-title">{{item.title}}</h5>
          <p class="card-text">{{item.Price}}</p>
          <a @click="addToCart(item)" class="btn btn-primary">Added</a>
        </div>
</div>

</div>



</div>
</template>

<script>


export default {
props:['items'],
methods:{
  addToCart(item){
    this.$emit('newItemAdded', item)
  }
}
}
</script>

<style>

</style>
