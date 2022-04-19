       <template>
  <div>
    <div class="grid grid-cols-12 gap-2 px-3 pt-3">
      <div class="col-span-6 sm:col-span-3">
        <label for="first-name" class="block text-sm font-medium text-gray-700"
          >Emitates Id
        </label>
        <input
          type="text"
          name="first-name"
          id="first-name"
          placeholder="Emitates Id"
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

      <div class="col-span-6 sm:col-span-3">
        <label for="last-name" class="block text-sm font-medium text-gray-700"
          >Current Visa</label
        >
        <input
          type="text"
          name="last-name"
          id="last-name"
          placeholder="Current Visa"
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

      <div class="col-span-6 sm:col-span-3">
        <PassportInput
          :removePassport="removePassport"
          v-on:openModal="openPassportModal()"
          :passportDetails="passportDetails"
        />
      </div>
      <div class="col-span-6 sm:col-span-3">
        <label
          for="date-of-birth"
          class="block text-sm font-medium text-gray-700"
          >License No</label
        >
        <input
          type="text"
          name="date-of-birth"
          placeholder="License No"
          id="date-of-birth"
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

      <div class="col-span-6 sm:col-span-3">
        <label
          for="date-of-birth"
          class="block text-sm font-medium text-gray-700"
          >Contract</label
        >
        <input
          type="text"
          name="date-of-birth"
          placeholder="Contract"
          id="date-of-birth"
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

      <div class="col-span-6 sm:col-span-3">
        <label
          for="date-of-birth"
          class="block text-sm font-medium text-gray-700"
          >Wps Number</label
        >
        <input
          type="text"
          name="date-of-birth"
          placeholder="Wps Number"
          id="date-of-birth"
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

      <div class="col-span-6 sm:col-span-3">
        <label
          for="date-of-birth"
          class="block text-sm font-medium text-gray-700"
          >Cost Center</label
        >
        <input
          type="text"
          name="date-of-birth"
          placeholder="Cost Center"
          id="date-of-birth"
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
          text-gray-700
          bg-white
          hover:bg-gray-50
          focus:outline-none
          focus:ring-2
          focus:ring-offset-2
          focus:ring-indigo-500
        "
        @click="goBack"
      >
        Back
      </button>
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
          focus:ring-indigo-500
        "
        @click="nextStep"
      >
        <!-- Heroicon name: solid/pencil -->

        Next
      </button>
    </div>
    <PassportModal
      v-on:addPassport="addPassport($event)"
      :toggleModal="toggleModal"
      v-if="showPassportModal"
    />
  </div>
</template>

<script>
import PassportInput from "~/components/EmployeeForm/PassportInput.vue";

export default {
  name: "Credential",
  components: {
    PassportInput,
  },
  props: ["nextStep", "goBack"],
  data() {
    return {
      passportDetails: { passportNo: 3621639182 },
      showPassportModal: false,
    };
  },

  methods: {
    async openPassportModal() {
      this.showPassportModal = true;
    },
    async removePassport() {
      alert("Are you sure! Remove Passport Details");
      this.passportDetails = { passportNo: "" };
    },
    async toggleModal() {
      this.showPassportModal = !this.showPassportModal;
    },
    async addPassport(values) {
      this.passportDetails = values;
      this.showPassportModal = false;
    },
  },
};
</script>