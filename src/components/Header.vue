<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container" id="my-nav">
      <a class="navbar-brand" href="#">Navbar</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item active">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
        </ul>
      </div>
    </div>
</nav>
</template>

<script>
export default {
  data(){
    return {

    }
  }
  
}
</script>


<style scoped>
  #my-nav{
    padding: 0 100px;
  }
</style>
