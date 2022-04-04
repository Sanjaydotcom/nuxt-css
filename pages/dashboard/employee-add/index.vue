<template>
  <div class="container mx-auto px-2 py-2">
    <PageHeader header="Add Employee"  />
  
    <EmployeeForm />


  </div>
</template>

<script>
import PageHeader from "~/components/PageHeader";
import Employees from "~/components/Employees";
import EmployeeForm from '~/components/EmployeeForm';

export default {
  name: "Employee-add",
  layout: "app",
  components: {
    PageHeader,
    Employees,
    EmployeeForm
  },
};
</script>

<style>
</style>