<template>
    <h1 v-if="show">Main Heading</h1>
    <button v-on:click="display">hide</button>
    <h3>Sub Heading</h3>
    <p id="para">Lorem ipsum dolor s</p>
    <span id="test"></span>
    <button v-on:mouseleave="hello">event</button>

    <table>
        <thead>
            <tr><th>id</th>
        <th>name</th>
        <th>phone</th></tr></thead>
        <tbody>
            <tr v-for="user in users" :key="user.id">
<td>{{ user.id }}</td>
<td>{{ user.name }}</td>
<td>{{ user.phone }}</td>

            
            </tr>
        </tbody>
    </table>
</template>

<script>
export default {
  name: 'HomeP',
  data(){
    return{
        users:[
            {id:1,name:'jon',phone:12345},
            {id:1,name:'jon',phone:12345},
            {id:1,name:'jon',phone:12345},
        ]
        
    }
  },
  methods:{
    hello(){
        alert("hi this is testing")
        
    },
    display(){
        this.show=!this.show

    }
   
  }

 
}
</script>