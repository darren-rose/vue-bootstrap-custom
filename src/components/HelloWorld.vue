<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="alert alert-primary" role="alert">
      This is a primary alert—check it out!
    </div>
    <button type="button" class="btn btn-primary">Primary</button>
    <button type="button" class="btn btn-secondary">Secondary</button>

  <div>
    <b-dropdown id="dropdown-1" text="Dropdown Button" class="m-md-2">
      <b-dropdown-item>First Action</b-dropdown-item>
      <b-dropdown-item>Second Action</b-dropdown-item>
      <b-dropdown-item>Third Action</b-dropdown-item>
      <b-dropdown-divider></b-dropdown-divider>
      <b-dropdown-item active>Active action</b-dropdown-item>
      <b-dropdown-item disabled>Disabled action</b-dropdown-item>
    </b-dropdown>
  </div>

  <div>
    <b-button @click="toggle" size="sm">
      {{ show ? 'Hide' : 'Show' }} Alert
    </b-button>
    <b-alert v-model="show"
            dismissible
            @dismissed="dismissed"
            class="mt-3">
      Hello {{ name }}!
    </b-alert>
  </div>

  <div class="container mt-3">

    <h2>Carousel</h2>
    <div id="myCarousel" class="carousel slide" data-ride="carousel">

      <!-- Indicators -->
      <ul class="carousel-indicators">
        <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
        <li data-target="#myCarousel" data-slide-to="1"></li>
        <li data-target="#myCarousel" data-slide-to="2"></li>
      </ul>
      
      <!-- The slideshow -->
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="https://cdn2.lamag.com/wp-content/uploads/sites/6/2017/01/LABridgeShutterstock2.jpg" alt="Los Angeles" width="1100" height="500">
        </div>
        <div class="carousel-item">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5f/Chicago_from_North_Avenue_Beach_June_2015_panorama_2.jpg/1340px-Chicago_from_North_Avenue_Beach_June_2015_panorama_2.jpg" alt="Chicago" width="1100" height="500">
        </div>
        <div class="carousel-item">
          <img src="https://media-cdn.tripadvisor.com/media/photo-s/0e/9a/e3/1d/freedom-tower.jpg" alt="New York" width="1100" height="500">
        </div>
      </div>
      
      <!-- Left and right controls -->
      <a class="carousel-control-prev" href="#myCarousel" data-slide="prev">
        <span class="carousel-control-prev-icon"></span>
      </a>
      <a class="carousel-control-next" href="#myCarousel" data-slide="next">
        <span class="carousel-control-next-icon"></span>
      </a>
    </div>

  </div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      name: 'BootstrapVue',
      show: true
    }
  },  
  methods: {
    toggle () {
      console.log('Toggle button clicked')
      this.show = !this.show
    },
    dismissed () {
      console.log('Dismiss button clicked')
    }
  }  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
