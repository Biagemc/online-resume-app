<template>
  <div id="app">
    <div id="nav">
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">Team API Project</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="/">Home <span class="sr-only">(current)</span></a>
      </li>
      
      <li class="nav-item">
        <a v-if="isLoggedIn()" class="nav-link disabled" href="/login">Login</a>
      </li>
      <li class="nav-item">
        <a v-if="isLoggedIn()" class="nav-link disabled" href="/logout">Logout</a>
      </li>
      <li class="nav-item">
        <a v-if="isLoggedIn()" class="nav-link disabled" href="/signup">Signup</a>
      </li>
    </ul>
    <form class="form-inline my-2 my-lg-0">
      <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
      <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
    </form>
  </div>
</nav>    </div>
    <router-view/>
  </div>
  
</template>
<script>
export default {
  methods: {
    isLoggedIn: function() {
      // console.log('i am checking login status');
      if (localStorage.getItem('jwt')) {
        return true;
      } else {
        return false;
      }
    },
  }
};

</script>
<style>


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
