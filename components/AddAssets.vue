<template>
  <div
    class="fixed z-10 inset-0 overflow-y-auto"
    aria-labelledby="modal-title"
    role="dialog"
    aria-modal="true"
  >
    <div
      class="
        flex
        items-end
        justify-center
        min-h-screen
        pt-4
        px-4
        pb-20
        text-center
        sm:block sm:p-0
      "
    >
      <!--
      Background overlay, show/hide based on modal state.

      Entering: "ease-out duration-300"
        From: "opacity-0"
        To: "opacity-100"
      Leaving: "ease-in duration-200"
        From: "opacity-100"
        To: "opacity-0"
    -->
      <div
        class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity"
        aria-hidden="true"
      ></div>

      <!-- This element is to trick the browser into centering the modal contents. -->
      <span
        class="hidden sm:inline-block sm:align-middle sm:h-screen"
        aria-hidden="true"
        >&#8203;</span
      >

      <!--
      Modal panel, show/hide based on modal state.

      Entering: "ease-out duration-300"
        From: "opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95"
        To: "opacity-100 translate-y-0 sm:scale-100"
      Leaving: "ease-in duration-200"
        From: "opacity-100 translate-y-0 sm:scale-100"
        To: "opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95"
    -->
      <div
        class="
          relative
          inline-block
          align-bottom
          bg-white
          rounded-lg
          px-2
          pt-5
          pb-4
          text-left
          overflow-hidden
          shadow-xl
          transform
          transition-all
          sm:my-8 sm:align-middle sm:max-w-md sm:w-full sm:p-6
        "
      >
        <div>
          <div class="mb-2 mt-2">
            <h3
              class="text-lg leading-6 font-medium text-center text-gray-900"
              id="modal-title"
            >
              Add Assets
            </h3>
            <div class="grid grid-cols-12 px-4 pt-4 gap-2">
              <div class="col-span-12">
                <label
                  for="asset-type"
                  class="block text-sm font-medium text-gray-700"
                  >Asset Code</label
                >
                <input
                  type="text"
                  name="first-name"
                  id="first-name"
                  placeholder="Passport Number"
                  autocomplete="given-name"
                  class="
                    mt-1
                    focus:ring-indigo-500 focus:border-indigo-500
                    block
                    w-full
                    shadow-sm
                    sm:text-sm
                    border-gray-300
                    rounded-md
                  "
                />
              </div>
              <div class="col-span-12">
                <label
                  for="blood-group"
                  class="block text-sm font-medium text-gray-700"
                  >Asset Type</label
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
                    focus:outline-none
                    focus:ring-indigo-500
                    focus:border-indigo-500
                    sm:text-sm
                  "
                >
                  <option>Option 1</option>
                  <option>Option 2</option>
                </select>
              </div>
              <div class="col-span-12">
                <label
                  for="last-name"
                  class="block text-sm font-medium text-gray-700"
                  >Issue Date</label
                >
                <input
                  type="date"
                  name="last-name"
                  id="last-name"
                  placeholder="Issue Date"
                  autocomplete="family-name"
                  class="
                    mt-1
                    focus:ring-indigo-500 focus:border-indigo-500
                    block
                    w-full
                    shadow-sm
                    sm:text-sm
                    border-gray-300
                    rounded-md
                  "
                />
              </div>
              <div class="col-span-12">
                <label
                  for="blood-group"
                  class="block text-sm font-medium text-gray-700"
                  >Status</label
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
                    focus:outline-none
                    focus:ring-indigo-500
                    focus:border-indigo-500
                    sm:text-sm
                  "
                >
                  <option>Option 1</option>
                  <option>Option 2</option>
                </select>
              </div>
            </div>
          </div>
        </div>
        <div
          class="
            mt-5 mx-5
            sm:mt-6 sm:grid sm:grid-cols-2 sm:gap-3 sm:grid-flow-row-dense
          "
        >
          <button
            type="button"
            @click="toggleModal"
            class="
              w-full
              inline-flex
              justify-center
              rounded-md
              border border-transparent
              shadow-sm
              px-4
              py-2
              bg-indigo-600
              text-base
              font-medium
              text-white
              hover:bg-indigo-700
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-500
              sm:col-start-2 sm:text-sm
            "
          >
            Save
          </button>
          <button
            type="button"
            @click="toggleModal"
            class="
              mt-3
              w-full
              inline-flex
              justify-center
              rounded-md
              border border-gray-300
              shadow-sm
              px-4
              py-2
              bg-white
              text-base
              font-medium
              text-gray-700
              hover:bg-gray-50
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-500
              sm:mt-0 sm:col-start-1 sm:text-sm
            "
          >
            Cancel
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: ["toggleModal"],
};
</script>