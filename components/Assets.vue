 <template>
  <div class="-my-2 -mx-4 overflow-x-auto sm:-mx-6 lg:-mx-8">
    <div class="grid grid-cols-12 gap-4 mt-3 py-3 pl-8">
      <div class="col-span-12 md:col-span-6 lg:col-span-3">
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
      <div class="col-span-12 self-end md:col-span-6 lg:col-span-3">
        <button
          type="button"
          class="
            inline-flex
            items-center
            px-4
            py-2
            border border-gray-300
            rounded-md
            shadow-sm
            text-sm
            font-medium
            text-gray-700
            bg-white
            hover:bg-gray-50
            focus:outline-none
            focus:ring-2
            focus:ring-offset-2
            focus:ring-indigo-400
          "
          @click="toggleModal"
        >
          <!-- Heroicon name: solid/pencil -->

          Add Assets
        </button>
      </div>
    </div>
    <div class="inline-block min-w-full py-2 align-middle md:px-6 lg:px-8">
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
                Asset Type
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
                Asset Code
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
                Issue Date
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
              <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                {{ item.assetType }}
              </td>

              <td class="whitespace-nowrap py-3 pl-4 text-sm sm:pl-6">
                <div class="flex items-center">
            
                  <div class="ml-4">
                    <div class="font-medium text-gray-600">{{ item.code }}</div>
                  </div>
                </div>
              </td>

              <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                <div class="text-gray-500">{{ item.date }}</div>
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
    <AddAssets :toggleModal="toggleModal" v-if="showmodal" />
  </div>
</template>

<script>
export default {
  name: "Assets",
  data() {
    return {
      searchQuery: "",
      showmodal: false,
      listItems: [
        {
          id: 1,
          assetType: "Asset One",
          code: "AC100",
          date: "12/02/2020",
          status: "Active",
        },
        {
          id: 2,
          assetType: "Asset two",
          code: "AC100",
          date: "08/04/2020",
          status: "Active",
        },
        {
          id: 3,
          assetType: "Asset three",
          code: "AC100",
          date: "20/07/2021",
          status: "Active",
        },
        {
          id: 4,
          assetType: "Asset four",
          code: "AC100",
          date: "17/09/2021",
          status: "Active",
        },
        {
          id: 5,
          assetType: "Asset five",
          code: "AC100",
          date: "28/02/2019",
          status: "Active",
        },
      ],
    };
  },
  methods: {
    async toggleModal() {
      this.showmodal = !this.showmodal;
    },
  },
  computed: {
    filteredRows() {
      return this.listItems.filter((row) => {
        const employees = row.assetType.toString().toLowerCase();
        const searchTerm = this.searchQuery.toLowerCase();

        return employees.includes(searchTerm);
      });
    },
  },
};
</script>