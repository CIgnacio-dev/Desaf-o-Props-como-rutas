<template>
  <div>
    <nav class="navbar navbar-light navbar-expand-lg fixed-top" id="mainNav">
        <div class="container"><a class="navbar-brand">V8</a><button data-toggle="collapse" data-target="#navbarResponsive" class="navbar-toggler" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation"><i class="fa fa-bars"></i></button>
          <div class="collapse navbar-collapse" id="navbarResponsive">
            
            <ul class="nav navbar-nav ml-auto" id="menu-v8">
                <li class="nav-item" role="presentation">
               
                  <router-link :to="{name: 'index'}">Portada</router-link>
                </li>
                <li class="nav-item" role="presentation">
                
                  <router-link :to="{name: 'SobreMi'}">Sobre Mí</router-link>
                </li>
                <li class="nav-item" role="presentation">
               
                  <router-link :to="{name: 'Contact'}">Contacto</router-link>
                </li>
                <li class="nav-item" role="presentation">
                
                  <router-link to="/post/1/article">Post</router-link> 
                </li>
                <li class="nav-item" role="presentation">
                
                  <router-link to="/administrador/simple">Administrador</router-link> 
                </li>
            </ul> 
        </div>
      </div>
    </nav>
    <transition name='opacity'>
      <router-view></router-view>
    </transition>
    
  </div>
  
</template>

<script>

export default {

}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;  
}
#menu-v8 a{
  text-shadow: 1px 1px #000;
}
.opacity-enter, .opacity-leave-to {
  opacity: 0;
}
.opacity-enter-to, .opacity-leave {
  opacity: 1;
}
.opacity-enter-active, .opacity-leave-active {
  transition: opacity 1s;
}
</style>
