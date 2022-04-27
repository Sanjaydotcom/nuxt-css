       <template>
  <div>
    <div class="grid grid-cols-12 gap-2 px-3 pt-2">
      <div class="col-span-6 sm:col-span-3">
        <label for="first-name" class="block text-sm font-medium text-gray-600"
          >First name</label
        >
        <input
          type="text"
          name="first-name"
          id="first-name"
          placeholder="First name"
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
        <label for="last-name" class="block text-sm font-medium text-gray-600"
          >Last name</label
        >
        <input
          type="text"
          name="last-name"
          id="last-name"
          placeholder="Last name"
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
        <label for="country" class="block text-sm font-medium text-gray-600"
          >Gender</label
        >
        <select
          id="country"
          name="country"
          autocomplete="country-name"
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
          <option>Male</option>
          <option>Female</option>
          <option>Others</option>
        </select>
      </div>
      <div class="col-span-6 sm:col-span-2">
        <label
          for="date-of-birth"
          class="block text-sm font-medium text-gray-600"
          >Date of Birth</label
        >
        <input
          type="date"
          name="date-of-birth"
          placeholder="Date of Birth"
          id="date-of-birth"
          autocomplete="given-name"
          class="
            mt-1
            focus:ring-indigo-400 focus:border-indigo-400
            block
            w-full
            shadow-sm
            h-38px
            sm:text-sm
            border-gray-300
            rounded-md
          "
        />
      </div>
      <div class="col-span-6 sm:col-span-2">
        <label for="blood-group" class="block text-sm font-medium text-gray-600"
          >Blood group</label
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
          <option>O-</option>
          <option>A+</option>
        </select>
      </div>
      <div class="col-span-6 sm:col-span-2">
        <label
          for="martial-status"
          class="block text-sm font-medium text-gray-600"
          >Martial Status</label
        >
        <select
          id="martial-status"
          name="martial-status"
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
          <option>Single</option>
          <option>Option 1</option>
          <option>Option 2</option>
        </select>
      </div>
      <div class="col-span-6 sm:col-span-3">
        <label for="nationality" class="block text-sm font-medium text-gray-600"
          >Nationality</label
        >
        <input
          type="text"
          placeholder="Nationality"
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
  name: "General",
  props: ["nextStep"],
};
</script>