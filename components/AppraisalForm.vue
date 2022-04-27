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
          px-4
          pt-5
          pb-4
          text-left
          overflow-hidden
          shadow-xl
          transform
          transition-all
          sm:my-8 sm:align-middle sm:max-w-2xl
          lg:w-full
          sm:p-6
        "
      >
        <div>
          <div class="mt-3 sm:mt-5">
            <h3
              class="text-md leading-6 font-small text-gray-900"
              id="modal-title"
            >
              Employee Appraisal
            </h3>
            <div class="mt-2">
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
                      Designation
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
                      Department
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
                      Amount
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
                      Date
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
                  <tr>
                    <td
                      class="whitespace-nowrap px-3 py-3 text-sm text-gray-500"
                    >
                      Designation One
                    </td>
                    <td
                      class="whitespace-nowrap px-3 py-3 text-sm text-gray-500"
                    >
                      Finacial
                    </td>
                    <td
                      class="whitespace-nowrap px-3 py-3 text-sm text-gray-500"
                    >
                      72528
                    </td>
                    <td
                      class="whitespace-nowrap px-3 py-3 text-sm text-gray-500"
                    >
                      <div class="text-gray-500">22/03/2022</div>
                    </td>
                    <td
                      class="whitespace-nowrap px-3 py-3 text-sm text-gray-500"
                    >
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
                        >Active</span
                      >
                    </td>

                   
                  </tr>
                </tbody>
              </table>
              <div class="my-3">
                <h3 class="text-md leading-6 font-small text-gray-900">
                  Appraisal Details
                </h3>
                <div class="grid grid-cols-12 px-4 pt-4 gap-2">
                  <div class="col-span-6">
                    <label
                      for="asset-type"
                      class="block text-sm font-medium text-gray-600"
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
                  <div class="col-span-6">
                    <label
                      for="blood-group"
                      class="block text-sm font-medium text-gray-600"
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
                        focus:outline-none
                        focus:ring-indigo-400
                        focus:border-indigo-400
                        sm:text-sm
                      "
                    >
                      <option>Option 1</option>
                      <option>Option 2</option>
                    </select>
                  </div>
                     <div class="col-span-6">
                    <label
                      for="blood-group"
                      class="block text-sm font-medium text-gray-600"
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
                        focus:outline-none
                        focus:ring-indigo-400
                        focus:border-indigo-400
                        sm:text-sm
                      "
                    >
                      <option>Option 1</option>
                      <option>Option 2</option>
                    </select>
                  </div>
                    <div class="col-span-6">
                    <label
                      for="blood-group"
                      class="block text-sm font-medium text-gray-600"
                      >Type of Appraisal</label
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
                        focus:ring-indigo-400
                        focus:border-indigo-400
                        sm:text-sm
                      "
                    >
                      <option>Option 1</option>
                      <option>Option 2</option>
                    </select>
                  </div>
                  <div class="col-span-6">
                    <label
                      for="last-name"
                      class="block text-sm font-medium text-gray-600"
                      >Date of Appraisal</label
                    >
                    <input
                      type="date"
                      name="last-name"
                      id="last-name"
                      placeholder="Date of Appraisal"
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
                  <div class="col-span-6">
                    <label
                      for="blood-group"
                      class="block text-sm font-medium text-gray-600"
                      >Amount</label
                    >
                    <input
                      type="text"
                      name="first-name"
                      id="first-name"
                      placeholder="Amount"
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
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="
            mt-5
            sm:mt-6 sm:grid sm:grid-cols-2 sm:gap-3 sm:grid-flow-row-dense
          "
        >
          <button
            type="button"
            @click="saveForm"
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
              focus:ring-indigo-400
              sm:col-start-2 sm:text-sm
            "
          >
            Save
          </button>
          <button
            @click="toggleModal"
            type="button"
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
              text-gray-600
              hover:bg-gray-50
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-400
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
  name: "AppraisalForm",
  props: ["toggleModal","saveForm"],
};
</script>