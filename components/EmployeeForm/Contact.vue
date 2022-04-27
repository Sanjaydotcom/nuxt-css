       <template>
  <div>
    <div class="grid grid-cols-12 gap-2 px-3 pt-3">
      <div class="col-span-6 sm:col-span-3">
        <label for="first-name" class="block text-sm font-medium text-gray-600"
          >Primary Contact Number</label
        >
        <input
          type="text"
          name="first-name"
          id="first-name"
          placeholder="Primary Contact Number"
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
          >Secondary Contact Number</label
        >
        <input
          type="text"
          name="last-name"
          id="last-name"
          placeholder="Secondary Contact Number"
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

      <div class="col-span-6 sm:col-span-3">
        <label
          for="date-of-birth"
          class="block text-sm font-medium text-gray-600"
          >Company Mail</label
        >
        <input
          type="text"
          name="date-of-birth"
          placeholder="Company Mail"
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

      <div class="col-span-6 sm:col-span-3">
        <label for="nationality" class="block text-sm font-medium text-gray-600"
          >Personal Mail</label
        >
        <input
          type="text"
          placeholder="Personal Mail"
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
      >
        <!-- Heroicon name: solid/pencil -->

        Back</button
      >
      
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
  name: "Contact",
  props: ["nextStep", "goBack"],
};
</script>