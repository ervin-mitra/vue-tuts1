<template>
  <div id="employee-table">
    <table>
      <thead>
        <tr>
          <th>Employee name</th>
          <th>Employee email</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="employee in employees" :key="employee.id">
            <td>{{ employee.name }}</td>
            <td>{{ employee.id }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<employee-table v-bind:employees="employees" />

<script>
  export default {
    name: 'employee-table',
    props: {
        employees: Array,
    },
  }
</script>

<style scoped></style>