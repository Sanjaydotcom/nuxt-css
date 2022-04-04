<template>
  <div
    :class="
      sidebarOpen ? 'translate-x-0 ease-out' : '-translate-x-full ease-in'
    "
    class="
      fixed
      z-30
      inset-y-0
      left-0
      w-64
      transition
      duration-300
      transform
      bg-white
      overflow-y-auto
      border-r-2
      lg:translate-x-0 lg:static lg:inset-0
    "
  >
    <div class="flex items-center justify-center mt-28">
      <div class="flex items-center bg-gray-100 p-6 rounded-xl">
        <div class="flex-shrink-0 h-10 w-10">
          <img
            class="h-10 w-10 rounded-full"
            src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
            alt=""
          />
        </div>

        <div class="ml-4">
          <div class="text-sm leading-5 font-medium text-gray-900">
            Sanjay Ns
          </div>
          <div class="text-sm leading-5 text-gray-500">Software Developer</div>
        </div>
      </div>
    </div>

    <nav class="mt-16">
      <a class="flex items-center py-4 px-6 bg-green-100 text-red-500" href="/dashboard">
        <svg
          class="h-6 w-6"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M11 3.055A9.001 9.001 0 1020.945 13H11V3.055z"
          ></path>
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M20.488 9H15V3.512A9.025 9.025 0 0120.488 9z"
          ></path>
        </svg>

        <span class="mx-3">Dashboard</span>
      </a>

      <a
        class="
          flex
          items-center
          py-4
          px-6
          text-gray-500
          hover:bg-green-100 hover:bg-opacity-25 hover:text-red-500
        "
        href="/meeting"
      >
        <svg
          class="h-6 w-6"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M17 14v6m-3-3h6M6 10h2a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v2a2 2 0 002 2zm10 0h2a2 2 0 002-2V6a2 2 0 00-2-2h-2a2 2 0 00-2 2v2a2 2 0 002 2zM6 20h2a2 2 0 002-2v-2a2 2 0 00-2-2H6a2 2 0 00-2 2v2a2 2 0 002 2z"
          ></path>
        </svg>

        <span class="mx-3">Meetings</span>
      </a>

      
    </nav>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  props: ["sidebarOpen"]
};
</script>
