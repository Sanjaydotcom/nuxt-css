       <template>
  <div>

    <div class="grid grid-cols-12 gap-2 px-3 pt-3">
      <div class="col-span-6 sm:col-span-3">
        <label for="first-name" class="block text-sm font-medium text-gray-600"
          >Designation</label
        >
        <input
          type="text"
          name="first-name"
          id="first-name"
          placeholder="Designation"
          autocomplete="given-name"
          class="
            mt-1
            focus:ring-indigo-400 focus:border-indigo-400
            block
            w-full
            shadow-sm
            sm:text-sm
            border-gray-300
            rounded-md
          "
        />
      </div>
      <div class="col-span-6 sm:col-span-3">
        <label for="blood-group" class="block text-sm font-medium text-gray-600"
          >Branch</label
        >
        <select
          id="blood-group"
          name="blood-group"
          autocomplete="martial-status"
          class="
            mt-1
            block
            w-full
            py-2
            px-3
            border border-gray-300
            bg-white
            rounded-md
            shadow-sm
            focus:outline-none focus:ring-indigo-400 focus:border-indigo-400
            sm:text-sm
          "
        >
          <option>Option 1</option>
          <option>Option 2</option>
        </select>
      </div>
      <div class="col-span-6 sm:col-span-2">
        <label for="blood-group" class="block text-sm font-medium text-gray-600"
          >Division</label
        >
        <select
          id="blood-group"
          name="blood-group"
          autocomplete="martial-status"
          class="
            mt-1
            block
            w-full
            py-2
            px-3
            border border-gray-300
            bg-white
            rounded-md
            shadow-sm
            focus:outline-none focus:ring-indigo-400 focus:border-indigo-400
            sm:text-sm
          "
        >
          <option>Option 1</option>
          <option>Option 2</option>
        </select>
      </div>
      <div class="col-span-6 sm:col-span-2">
        <label for="blood-group" class="block text-sm font-medium text-gray-600"
          >Department</label
        >
        <select
          id="blood-group"
          name="blood-group"
          autocomplete="martial-status"
          class="
            mt-1
            block
            w-full
            py-2
            px-3
            border border-gray-300
            bg-white
            rounded-md
            shadow-sm
            focus:outline-none focus:ring-indigo-400 focus:border-indigo-400
            sm:text-sm
          "
        >
          <option>Option 1</option>
          <option>Option 2</option>
        </select>
      </div>
      <div class="col-span-6 sm:col-span-2">
        <label for="blood-group" class="block text-sm font-medium text-gray-600"
          >Reporting Manager</label
        >
        <select
          id="blood-group"
          name="blood-group"
          autocomplete="martial-status"
          class="
            mt-1
            block
            w-full
            py-2
            px-3
            border border-gray-300
            bg-white
            rounded-md
            shadow-sm
            focus:outline-none focus:ring-indigo-400 focus:border-indigo-400
            sm:text-sm
          "
        >
          <option>Option 1</option>
          <option>Option 2</option>
        </select>
      </div>
      <div class="col-span-6 sm:col-span-2">
        <label for="last-name" class="block text-sm font-medium text-gray-600"
          >Date of Joining</label
        >
        <input
          type="date"
          name="last-name"
          id="last-name"
          class="
            mt-1
            focus:ring-indigo-400 focus:border-indigo-400
            block
            w-full
            shadow-sm
            sm:text-sm
            border-gray-300
            rounded-md
          "
        />
      </div>

      <div class="col-span-6 sm:col-span-2">
        <label for="last-name" class="block text-sm font-medium text-gray-600"
          >Year of Service</label
        >
        <input
          type="text"
          name="last-name"
          id="last-name"
          placeholder="Year of Service"
          autocomplete="family-name"
          class="
            mt-1
            focus:ring-indigo-400 focus:border-indigo-400
            block
            w-full
            shadow-sm
            sm:text-sm
            border-gray-300
            rounded-md
          "
        />
      </div>

      <div class="col-span-6 sm:col-span-2">
        <label
          for="date-of-birth"
          class="block text-sm font-medium text-gray-600"
          >Gross Salary</label
        >
        <input
          type="text"
          name="date-of-birth"
          placeholder="Gross Salary"
          id="date-of-birth"
          autocomplete="given-name"
          class="
            mt-1
            focus:ring-indigo-400 focus:border-indigo-400
            block
            w-full
            shadow-sm
            sm:text-sm
            border-gray-300
            rounded-md
          "
        />
      </div>

      <div class="col-span-6 sm:col-span-2">
        <label for="nationality" class="block text-sm font-medium text-gray-600"
          >Allowance</label
        >
        <input
          type="text"
          placeholder="Allowance"
          name="nationality"
          id="nationality"
          autocomplete="family-name"
          class="
            mt-1
            focus:ring-indigo-400 focus:border-indigo-400
            block
            w-full
            shadow-sm
            sm:text-sm
            border-gray-300
            rounded-md
          "
        />
      </div>
    </div>
     <div class="flex justify-end px-2 pt-2">
     <button
        type="button"
        class="
          inline-flex
          items-center
          px-4
          py-2
          mx-3
          border border-gray-300
          rounded-md
          shadow-sm
          text-sm
          font-medium
          text-gray-600
          bg-white
          hover:bg-gray-50
          focus:outline-none
          focus:ring-2
          focus:ring-offset-2
          focus:ring-indigo-400
        "
        @click="goBack"
      >       Back</button
      ><button
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
          text-gray-600
          bg-white
          hover:bg-gray-50
          focus:outline-none
          focus:ring-2
          focus:ring-offset-2
          focus:ring-indigo-400
        "
        @click="nextStep"
      >
        <!-- Heroicon name: solid/pencil -->

        Next
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Employment",
  props: ["nextStep", "goBack"],


};
</script>