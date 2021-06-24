<template> 
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Yaw to Your Vue.js App"/> -->
    <!-- <h1>Fresh start</h1> -->
    <h1>{{ copy.title }}</h1>
    <small>{{ copy.subtitle }}</small>
    <p>{{ copy.introduction }}</p>
  </div> 

  <div class="projects-wrapper">
  <h2>My Past Projects:</h2>
  <article v-for="project in projects" :key="project.title">
  <h3>{{ project.title}}</h3>
  <img :src="project.image" alt="photo for the project">

  <p>{{ p.description }}</p>

  <h4>tech used:</h4>

  <ul>
  <li v-for="tech om project.techStack" :key="tech">{{ tech }}</li>
  </ul>

  {{JSON.stringify(project)}}
  
  </article>
  </div>
</template>

<!-- <script> 
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script> -->

<script>

const STACK_OPTIONS ={
  PHP: "Php",
  VUE: "Vue.js",
  Node: "Node.js"

};

export default{
  name: "PortfolioApp",
  data: () => ({
    projects:  [
  {
    title: "Online Food Store",
    image: "https://i.ibb.co/ph6x1mq/2650401.jpg",
    description: "An online store that enables customers to buy food from resellers.",
    techStack: [
      STACK_OPTIONS.VUE,
      STACK_OPTIONS.PHP
    ]
  },
        {
    title: "Shares in Bitcoin",
    image: "https://i.ibb.co/ph6x1mq/2650401.jpg",
    description: "A page for viewing share prices in Bitcoin.",
    techStack: [
      STACK_OPTIONS.VUE,
      STACK_OPTIONS.NODE
    ]
  }
]
  }),


};

</script>

<style> 
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
