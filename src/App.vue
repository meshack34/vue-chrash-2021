<template>
<div class="container">
<Header title= "Track Traker"/>
<Tasks v-bind:tasks= "tasks"/>
</div>


  
</template> 

<script>
import Header from './components/Header'
import Tasks from './components/Tasks'
export default {
  name: 'App',
  components: {
    Header,
    Tasks, 
  },

  data(){
    return{
      tasks: []
    }
  },
  created(){
    this.tasks=[
      {
          id:1,
          text:"Doctors",
          day:"march 5th at 1;30PM",
          reminder:true,
        },
        {
          id:2,
          text:"food  sho",
          day:"march 4th at 11a.m",
          reminder:true,
        },
        {
          id:3,
          text:"meeting at school",
          day:"march 8 at 3;60PM",
          reminder:false,
        },
        {
          id:4,
          text:"monday",
          day:"march 8 at 3;00a.m",
          reminder:true,
        },
    ]
  },

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
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
