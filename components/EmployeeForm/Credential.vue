       <template>
  <div>
    <div class="grid grid-cols-12 gap-2 px-3 pt-3">
      <div class="col-span-6 sm:col-span-3">
        <label for="first-name" class="block text-sm font-medium text-gray-600"
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
        <VisaInput
          :removeVisa="removeVisa"
          v-on:openModal="openVisaModal()"
          :visaDetails="visaDetails"
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
          class="block text-sm font-medium text-gray-600"
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
    <PassportModal
      v-on:addPassport="addPassport($event)"
      :toggleModal="toggleModal"
      v-if="showPassportModal"
    />
     <VisaModal
      v-on:addVisa="addVisa($event)"
      :toggleModal="toggleVisaModal"
      v-if="showVisaModal"
    />
  </div>
</template>

<script>
import PassportInput from "~/components/EmployeeForm/PassportInput.vue";
import VisaInput from "~/components/EmployeeForm/VisaInput.vue";

export default {
  name: "Credential",
  components: {
    PassportInput,
    VisaInput
  },
  props: ["nextStep", "goBack"],
  data() {
    return {
      passportDetails: { passportNo: 3621639182 },
      visaDetails: { visaNo: 2193617892 },
      showPassportModal: false,
      showVisaModal: false,
    };
  },

  methods: {
    async openPassportModal() {
      this.showPassportModal = true;
    },
      async openVisaModal() {
      this.showVisaModal = true;
    },

    async removePassport() {
      alert("Are you sure! Remove Passport Details");
      this.passportDetails = { passportNo: "" };
    },
    async removeVisa() {
      alert("Are you sure! Remove Visa Details");
      this.visaDetails = { visaNo: "" };
    },
    async toggleModal() {
      this.showPassportModal = !this.showPassportModal;
    },
    async toggleVisaModal() {
      this.showVisaModal = !this.showVisaModal;
    },
    async addPassport(values) {
      this.passportDetails = values;
      this.showPassportModal = false;
    },
    async addVisa(values) {
      this.visaDetails = values;
      this.showVisaModal = false;
    },
  },
};
</script>