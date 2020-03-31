 <template>
<div id="app">
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Sumon store</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">


    <form @submit.prevent="surch" class="form-inline my-2 my-lg-0">
      <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
      <button class="btn btn-outline-success my-2 my-sm-0" type="submit" v-bind="keyword">Search</button>
    </form>
  </div>
</nav>



</div>
</template>

<script>


export default {
  data:{
    return: {
      keyword: ''
    }
  },
methods:{
  surch(){
    this.$$emit('surch', this.keyword)
  }
}
}
</script>

<style>
.container{
  padding: 10px;
}
</style>
