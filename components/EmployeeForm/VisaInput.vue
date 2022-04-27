<template>
  <div>
    <div v-on:click="$emit('openModal')" v-if="!visaDetails.visaNo">
      <label for="date-of-birth" class="block text-sm font-medium text-gray-600"
        >Current Visa</label
      >
      <input
        type="text"
        name="date-of-birth"
        placeholder="Visa No"
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
    <div v-if="visaDetails.visaNo !== ''">
      <div
      @click="removeVisa()"
        class="
          relative
          mx-3
          my-rounded-lg
          rounded-md
          bg-gray-100
          px-6
          py-3
          shadow-sm
          flex
          items-center
          space-x-3
          hover:border-gray-200
        "
      >
        <button
          
          type="button"
          class="absolute top-1 right-1 text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">Close</span>
          <!-- Heroicon name: outline/x -->
          <svg
            class="h-4 w-4"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            aria-hidden="true"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
        <div class="flex-1 min-w-0">
          <a href="#" class="focus:outline-none">
            <span class="absolute inset-0" aria-hidden="true"></span>
            <p class="text-sm font-medium text-gray-900">
              {{ visaDetails.visaNo }}
            </p>
            <p class="text-xs text-gray-500 truncate">Visa Details</p>
          </a>
        </div>
        <div class="flex-shrink-0">
          <button
            type="button"
            class="
              inline-flex
              items-center
              px-4
              py-1
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
            More
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from "~/components/Modal";

export default {
  name: "VisaInput",
  components: {
    Modal,
  },

  props: {
    visaDetails: {
      type: Object,
    },
    removeVisa: {
        type: Function
      }
    
  },
  data() {
    return {
      showmodal: false,
    };
  },

  methods: {
    async openModal() {
      this.showmodal = true;
    },

    // Define a method that Vue will call to handle the 'update' event.
    async toggleModal() {
      this.showmodal = !this.showmodal;
    },
  },
};
</script>