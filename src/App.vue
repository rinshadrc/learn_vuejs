<template>

  <div id="app">

    <!-- <MainPage /> -->

 
  <employee-form @add:employee="newEmployee"/>
  <employee-table v-bind:employees="employees" />
</div>
</template>

<script>
import EmployeeForm from './components/EmployeeForm.vue';
// import MainPage from './components/Main.vue';
import EmployeeTable from './components/EmployeeTable.vue';



export default {
  name: 'App',
  components: {
    // MainPage,
    EmployeeTable,
    EmployeeForm
  },
  data(){
    return{
      employees :[
        // {
        //   name:'akshay',email:'ak@g.com'
        // },
        // {
        //   name:'shamil',email:'sml@g.com'
        // },
        // {
        //   name:'ram',email:'rsm@g.com'
        // }
      ]
    }
  
},
methods:{
  newEmployee(employee){


    // 3 dot means exist data in employees array employee added to this employees array

    this.employees=[...this.employees,employee]

  }
}

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin: 50px;
}

.logo {
  height: 300px;
}
</style>
