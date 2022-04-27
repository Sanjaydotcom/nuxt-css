       <template>
  <div>

      <div class="grid grid-cols-12 gap-2 px-3 pt-3">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-600"
            >Name</label
          >
          <input
            type="text"
            name="first-name"
            id="first-name"
            placeholder="Name"
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
            >Reference Type</label
          >
          <input
            type="text"
            name="last-name"
            id="last-name"
            placeholder="Reference Type"
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
            for="first-name"
            class="block text-sm font-medium text-gray-600"
            >Contact No</label
          >
          <input
            type="text"
            name="first-name"
            id="first-name"
            placeholder="Contact No"
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
          <label for="last-name" class="block text-sm font-medium text-gray-600"
            >Email</label
          >
          <input
            type="text"
            name="last-name"
            id="last-name"
            placeholder="Email"
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
          <button
            type="button"
            @click="toggleModal"
            class="
              inline-flex
              mt-6
              justify-center
              py-2
              px-4
              border
              shadow-sm
              text-sm
              border-gray-300
              font-medium
              rounded-md
              text-gray-600
              bg-white
              hover:bg-grey-700
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-400
            "
          >
            Add More
          </button>
        </div>
      </div>
        <div class="flex justify-end px-2">
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
      >      Back</button
      > <button
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
      
      >
        <!-- Heroicon name: solid/pencil -->

        Save
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "References",
   props: ["nextStep", "goBack"],


};
</script>