 <template>
  <div class="-my-2 -mx-4 overflow-x-auto sm:-mx-6 lg:-mx-8">
    <div class="inline-block min-w-full py-2 align-middle md:px-6 lg:px-8">
      <div class="grid grid-cols-12 gap-2 py-3">
        <div class="col-span-12 sm:col-span-3">
          <input
            type="text"
            name="search"
            id="search"
            v-model="searchQuery"
            placeholder="Enter your search here.."
            autocomplete="given-name"
            class="
              mt-1
              focus:ring-indigo-400 focus:border-indigo-400
              block
              w-full
              shadow-sm
              sm:text-sm
              bg-gray-100
              rounded-md
              border-none
            "
          />
        </div>
      </div>
      <div
        class="
          overflow-hidden
          shadow
          ring-1 ring-black ring-opacity-5
          md:rounded-lg
        "
      >
        <table class="min-w-full divide-y divide-gray-300">
          <thead class="bg-gray-50">
            <tr>
              <th
                scope="col"
                class="
                  px-3
                  py-3.5
                  text-left text-sm
                  font-semibold
                  text-gray-600
                "
              >
                Emploee Id
              </th>
              <th
                scope="col"
                class="
                  py-3.5
                  pl-4
                  pr-3
                  text-left text-sm
                  font-semibold
                  text-gray-600
                  sm:pl-6
                "
              >
                Name
              </th>
              <th
                scope="col"
                class="
                  px-3
                  py-3.5
                  text-left text-sm
                  font-semibold
                  text-gray-600
                "
              >
                Designation
              </th>
              <th
                scope="col"
                class="
                  px-3
                  py-3.5
                  text-left text-sm
                  font-semibold
                  text-gray-600
                "
              >
                Status
              </th>
              <th scope="col" class="relative py-3.5 pl-3 pr-4 sm:pr-6">
                <span class="sr-only">Edit</span>
              </th>
            </tr>
          </thead>
          <tbody class="divide-y divide-gray-200 bg-white">
            <tr v-for="item in filteredRows" :key="item.id">
              <td
                class="
                  whitespace-nowrap
                  px-3
                  py-3
                  font-medium
                  text-sm text-gray-500
                "
              >
                {{ item.emplyeeId }}
              </td>

              <td class="whitespace-nowrap py-3 pl-4 text-sm sm:pl-6">
                <div class="flex items-center">
                  <div class="h-10 w-10 flex-shrink-0">
                    <img
                      class="h-10 w-10 rounded-full"
                      src="https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                      alt=""
                    />
                  </div>
                  <div class="ml-4">
                    <div class="font-medium text-gray-700">{{ item.name }}</div>
                    <div class="text-gray-500">lindsay.walton@example.com</div>
                  </div>
                </div>
              </td>

              <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                <div class="text-gray-700">{{ item.designation }}</div>
                <div class="text-gray-500">{{ item.department }}</div>
              </td>
              <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                <span
                  class="
                    inline-flex
                    rounded-full
                    bg-green-100
                    px-2
                    text-xs
                    font-semibold
                    leading-5
                    text-green-800
                  "
                  >{{ item.status }}</span
                >
              </td>

              <td
                class="
                  relative
                  whitespace-nowrap
                  py-3
                  pl-3
                  pr-4
                  text-right text-sm
                  font-medium
                  sm:pr-6
                "
              >
                <a href="#" class="text-gray-600 hover:text-indigo-600"
                  ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-5 w-5"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z"
                    /></svg
                ></a>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Employees",
  data() {
    return {
      searchQuery: "",
      listItems: [
        {
          id: 1,
          emplyeeId: "EMP00001",
          name: "Sanjay",
          department: "Tech",
          status: "Active",
          designation: "Team Leader",
        },
        {
          id: 2,
          emplyeeId: "EMP00002",
          name: "Bhagath",
          department: "Accounts",
          status: "Active",
          designation: "Accounts Manger",
        },
        {
          id: 3,
          emplyeeId: "EMP00003",
          name: "Ajit",
          department: "Finance",
          status: "Active",
          designation: "Fianance Manger",
        },
        {
          id: 4,
          emplyeeId: "EMP00001",
          name: "Sharaf",
          department: "Tech",
          status: "Active",
          designation: "Team Leader",
        },
        {
          id: 5,
          emplyeeId: "EMP00002",
          name: "Arun",
          department: "Accounts",
          status: "Active",
          designation: "Accounts Manger",
        },
        {
          id: 6,
          emplyeeId: "EMP00003",
          name: "Ibrahim",
          department: "Finance",
          status: "Active",
          designation: "Fianance Manger",
        },
        {
          id: 7,
          emplyeeId: "EMP00001",
          name: "Sanjay",
          department: "Tech",
          status: "Active",
          designation: "Team Leader",
        },
      ],
    };
  },
  methods: {},
  computed: {
    filteredRows() {
      return this.listItems.filter((row) => {
        const employees = row.name.toString().toLowerCase();
        const searchTerm = this.searchQuery.toLowerCase();

        return employees.includes(searchTerm);
      });
    },
  },
};
</script>