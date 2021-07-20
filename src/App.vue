<template>
  <div class="container">
    
    <Header @toggle-add-task="toggleAddTask" title="Task Tracker" :showAddTask="showAddTask" />

    <router-view :showAddTask="showAddTask"></router-view>
    <Footer />
   
  </div>
</template>

<script>
import Header from "./components/Header";
import Footer from "./components/Footer";


export default {
  name: "App",
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      showAddTask: false,
    }
  },
  methods: {
     toggleAddTask(){
      this.showAddTask = !this.showAddTask
    },

}
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
    background-color: rgb(11, 255, 52);
  
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 5px solid rgb(221, 3, 3);
  padding: 40px;
  position: relative;
  border-radius: 1rem;
  background: rgba(247, 244, 79, 0.8);
  transform-style: preserve-3d;
  transition: 0.5s;
  box-shadow: 0 15px 35px rgba(248, 242, 242, 0.966);
    
}

.btn {
  display: inline-block;
  background: rgb(6, 44, 255);
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;

}
</style>
