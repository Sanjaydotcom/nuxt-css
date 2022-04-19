<template>
  <div class="container mx-auto px-2 py-2">
    <div class="flex justify-between mx-auto px-2 py-2">
      <PageHeader header="Employees" />

      <NuxtLink
        to="../dashboard/employee-add"
        class="
          ml-3
          h-10
          inline-flex
          items-center
          px-4
          py-1
          border border-transparent
          rounded-md
          shadow-sm
          text-sm
          font-medium
          text-gray-600
          bg-white
          hover:bg-gray-100
          focus:outline-none
          border-gray-300
          focus:ring-1
          focus:ring-offset-1
          focus:ring-indigo-500
        "
      >
       <svg class="ml-1 mr-2 h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
        <path fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z" clip-rule="evenodd" />
      </svg>  Add Employee
      </NuxtLink>
    </div>
    <div class="flex flex-col mt-8">
      <div class="-my-2 py-2 overflow-x-auto sm:-mx-6 sm:px-6 lg:-mx-8 lg:px-8">
        <Employees />
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
    Employees,
  },
};
</script>
