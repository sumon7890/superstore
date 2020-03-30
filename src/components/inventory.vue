<template>
<div id="app">
    <div class="row">
    <div v-for="(value, name, index) in items" :key="index" class="card" style="width: 14rem;">
      {{ index }}. {{ name }}: {{ value }}
          <!-- <img :src="item.photo" class="card-img-top" alt="Card Img">
        <div class="card-body">
          <h5 class="card-title">{{item.title}}</h5>
          <p class="card-text">{{item.price}}</p>
          <a href="#" class="btn btn-primary">Added</a>
        </div> -->
</div>

</div>



</div>
</template>

<script>


export default {
props:['items']
}
</script>

<style>

</style>
