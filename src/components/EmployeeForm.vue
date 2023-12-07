<template>
  <h1>Registration Form</h1>

    <form v-on:submit.prevent="addEmployee">
    <div class="mb-3">
      <label for="name" class="form-label">Name</label>
      <input type="text" class="form-control" id="name" v-model="employee.name">
    </div>
    <div class="mb-3">
      <label for="exampleInputEmail1" class="form-label">Email address</label>
      <input type="email" class="form-control" id="exampleInputEmail1" v-model="employee.email">
    </div>
   
   
    <button type="submit" class="btn btn-success">Add employee</button>
  </form>
</template>
<script>
export default {
    name:"employee-form",
    data(){
        return{
            employee:{

                name:'',
                email:''
            }
            
        }
    },
    methods:{
        addEmployee(){
            
            this.$emit('add:employee',this.employee );
            this.employee = { name: '', email: '' };
        }
    }
    
    
}
</script>