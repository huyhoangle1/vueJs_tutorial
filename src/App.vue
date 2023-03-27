<template>
  <div id="app">
    <div>
<h1 :class="{dachon : selected}"> Le Huy hoang</h1>
      <button @click="selected = ! selected">click</button>
    </div>
    <!-- <input type="text" v-model="newtask">
<button @click="addtask()">them</button> -->
          <input type="text" v-model="newtask">
      <button @click="tasks.push({content: newtask,done: false})">them</button>
    <div v-for="(task, index) in tasks" :key="index">
      <!-- {{task}} -->
      <input type="checkbox" v-model="task.done">
      <span :class="{done: task.done}">{{task.content}}</span>

    </div>
    <input type="text" v-model="name">
    <input type="checkbox" v-model="yes">tôi đồng ý điều khoản
    <input type="text" :disabled="inputDisable">
          <button @click="inputDisable = ! inputDisable"> ẩn/Hiện</button>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Menuhihi/>
    <!-- <div v-show="isShow">
      <h1>Lập trình viên hiển thị </h1></div> 
       <button @click="isShow = ! isShow"> ẩn/Hiện</button> -->

       <div v-if="isShow">  Lập trình viên hiển thị </div>
      <button @click="isShow =! isShow">
        <span v-if="isShow">an</span>
        <span v-else>hien</span>
      </button>
 <div> 
   {{name}}
 </div>
  </div>
  
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Menuhihi from './components/Menuhihi.vue'
export default {
  name: 'App',
  data(){
    return{
      newTask:' ',
      tasks:[
      {content: 'đi chơi',done:false},
      {content: 'nấu ăn',done:false},
      {content:'code',done:false},
      ],
      name : 'le huy hoang',
      yes :true,
      isShow:true,
      inputDisable:true,
      selected:true
    }
  },
  // methods: {
  //   addTask:function(){
  //     this.tasks.push({
  //       content: this.newTask,
  //       done: false
  //     });
  //   }
  // },
  // watch:{
  //   newTask: function(newvalue , oldvalue){
  //     console.log(newvalue);
  //     console.log(oldvalue);
  //   }
  // },
  mounted(){
    // goi IPa
  },
  components: {
    // HelloWorld,
    // Menuhihi
  }
}
</script>

<style>
.done{
  text-decoration:line-through;
}
.dachon{
  color: red;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
