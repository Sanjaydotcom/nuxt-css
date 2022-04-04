 <template><table class="min-w-full divide-y divide-gray-300">
            <thead class="bg-gray-50">
              <tr>
                <th scope="col" class="whitespace-nowrap py-3.5 pl-4 pr-3 text-left text-sm font-semibold text-gray-900 sm:pl-6">Employee ID</th>
                <th scope="col" class="whitespace-nowrap px-2 py-3.5 text-left text-sm font-semibold text-gray-900">Name</th>
                <th scope="col" class="whitespace-nowrap px-2 py-3.5 text-left text-sm font-semibold text-gray-900">Department</th>
                <th scope="col" class="whitespace-nowrap px-2 py-3.5 text-left text-sm font-semibold text-gray-900">Designation</th>
                <th scope="col" class="whitespace-nowrap px-2 py-3.5 text-left text-sm font-semibold text-gray-900">Status</th>

                <th scope="col" class="relative whitespace-nowrap py-3.5 pl-3 pr-4 sm:pr-6">
                  <span class="sr-only">Edit</span>
                </th>
              </tr>
            </thead>
            <tbody class="divide-y divide-gray-200 bg-white">
              <tr v-for="item in listItems" :key="item.id">
                <td class="whitespace-nowrap py-2 pl-4 pr-3 text-sm text-gray-500 sm:pl-6">{{ item.emplyeeId }}</td>
                <td class="whitespace-nowrap px-2 py-2 text-sm font-medium text-gray-900">C{{ item.name }}</td>
                <td class="whitespace-nowrap px-2 py-2 text-sm text-gray-900">{{ item.department }}</td>
                <td class="whitespace-nowrap px-2 py-2 text-sm text-gray-500">{{ item.designation }}</td>
                <td class="whitespace-nowrap px-2 py-2 text-sm text-gray-500"><span class="inline-flex rounded-full bg-green-100 px-2 text-xs font-semibold leading-5 text-green-800">{{ item.status }}</span></td>
                <td class="relative whitespace-nowrap py-2 pl-3 pr-4 text-right text-sm font-medium sm:pr-6">
                  <a href="#" class="text-indigo-600 hover:text-indigo-900">Edit<span class="sr-only">, AAPS0L</span></a>
                </td>
              </tr>

              <!-- More transactions... -->
            </tbody>
          </table>
 
</template>

<script>
export default {
  name: 'Employees',
 data() {
    return {
      listItems: [
        {
          id: 1,
          emplyeeId: "EMP00001",
          name: "Emplyee One",
          department: "Tech",
          status: "Active",
          designation: "Team Leader",
        },
       {
          id: 2,
          emplyeeId: "EMP00002",
          name: "Emplyee Two",
          department: "Accounts",
          status: "Active",
          designation: "Accounts Manger",
        },
         {
          id: 3,
          emplyeeId: "EMP00003",
          name: "Emplyee Two",
          department: "Finance",
          status: "Active",
          designation: "Fianance Manger",
        },
              {
          id: 4,
          emplyeeId: "EMP00001",
          name: "Emplyee One",
          department: "Tech",
          status: "Active",
          designation: "Team Leader",
        },
       {
          id: 5,
          emplyeeId: "EMP00002",
          name: "Emplyee Two",
          department: "Accounts",
          status: "Active",
          designation: "Accounts Manger",
        },
         {
          id: 6,
          emplyeeId: "EMP00003",
          name: "Emplyee Two",
          department: "Finance",
          status: "Active",
          designation: "Fianance Manger",
        },
              {
          id: 7,
          emplyeeId: "EMP00001",
          name: "Emplyee One",
          department: "Tech",
          status: "Active",
          designation: "Team Leader",
        },
       {
          id: 8,
          emplyeeId: "EMP00002",
          name: "Emplyee Two",
          department: "Accounts",
          status: "Active",
          designation: "Accounts Manger",
        },
         {
          id: 9,
          emplyeeId: "EMP00003",
          name: "Emplyee Two",
          department: "Finance",
          status: "Active",
          designation: "Fianance Manger",
        },
      ],
    };
  },
};
</script>
