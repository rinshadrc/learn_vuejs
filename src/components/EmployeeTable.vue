<template>
  <h1>Employees</h1>

    <table class="table">
        <thead class="table-dark">
            <tr >
                <th>Name</th>

                <th>Email</th>

            </tr>
        </thead>
        <tbody>
            <tr v-for="employee in employees" :key="employee.id">
                <td>{{ employee.name }}</td>
                <td>{{ employee.email }}</td>

            </tr>
        </tbody>
    </table>
</template>
<script>
export default {
    name:"employee-table",
    props:{
        employees:Array
    }
}
</script>