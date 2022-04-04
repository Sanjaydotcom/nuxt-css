<template>
  <div class="container mx-auto px-2 py-2">
  <div class="flex justify-between mx-auto px-2 py-2">
    <PageHeader header="Employees"  />
  
     <NuxtLink to="../dashboard/employee-add" class="ml-3 h-10 inline-flex items-center px-4 py-1 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
       Add Employee
        </NuxtLink> 
  
    </div>
    <div class="flex flex-col mt-8">
      <div class="-my-2 py-2 overflow-x-auto sm:-mx-6 sm:px-6 lg:-mx-8 lg:px-8">
        <div
          class="
            align-middle
            inline-block
            min-w-full
            shadow
            overflow-hidden
            sm:rounded-lg
            border-b border-gray-200
          "
        >
         <Employees />  
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PageHeader from "~/components/PageHeader";
import Employees from "~/components/Employees";

export default {
  name: "Dashboard",
  layout: "app",
  components: {
    PageHeader,
    Employees
  },
};
</script>

<style>
</style>