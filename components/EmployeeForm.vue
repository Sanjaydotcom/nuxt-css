 <template>
  <div class="mt-5 md:mt-0 md:col-span-2">
    <form action="#" method="POST">
      <div class="pt-4 pb-2">
        <h3 class="text-md leading-6 font-medium text-gray-900">
          General Details
        </h3>
      </div>
      <div class="grid grid-cols-12 gap-2">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
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
          <label for="country" class="block text-sm font-medium text-gray-700"
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>Male</option>
            <option>Female</option>
            <option>Others</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-3">
          <label
            for="date-of-birth"
            class="block text-sm font-medium text-gray-700"
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
            for="blood-group"
            class="block text-sm font-medium text-gray-700"
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>O-</option>
            <option>A+</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-3">
          <label
            for="martial-status"
            class="block text-sm font-medium text-gray-700"
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>Male</option>
            <option>Female</option>
            <option>Others</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-3">
          <label
            for="nationality"
            class="block text-sm font-medium text-gray-700"
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
      <div class="pt-4 pb-2">
        <h3 class="text-md leading-6 font-medium text-gray-900">
          Contact Details
        </h3>
      </div>
      <div class="grid grid-cols-12 gap-2">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
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
            >Company Mail</label
          >
          <input
            type="date"
            name="date-of-birth"
            placeholder="Company Mail"
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
            for="nationality"
            class="block text-sm font-medium text-gray-700"
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

      <div class="pt-4 pb-2">
        <h3 class="text-md leading-6 font-medium text-gray-900">
          Employment Details
        </h3>
      </div>
      <div class="grid grid-cols-12 gap-2">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
            >Designation</label
          >
          <input
            type="text"
            name="first-name"
            id="first-name"
            placeholder="Primary Contact Number"
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
            for="blood-group"
            class="block text-sm font-medium text-gray-700"
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>Option 1</option>
            <option>Option 2</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-3">
          <label
            for="blood-group"
            class="block text-sm font-medium text-gray-700"
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>Option 1</option>
            <option>Option 2</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-3">
          <label
            for="blood-group"
            class="block text-sm font-medium text-gray-700"
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>Option 1</option>
            <option>Option 2</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-3">
          <label
            for="blood-group"
            class="block text-sm font-medium text-gray-700"
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>Option 1</option>
            <option>Option 2</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-3">
          <label for="last-name" class="block text-sm font-medium text-gray-700"
            >Date of Joining</label
          >
          <input
            type="date"
            name="last-name"
            id="last-name"
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
            >Gross Salary</label
          >
          <input
            type="date"
            name="date-of-birth"
            placeholder="Gross Salary"
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
            for="nationality"
            class="block text-sm font-medium text-gray-700"
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
      <div class="pt-4 pb-2">
        <h3 class="text-md leading-6 font-medium text-gray-900">
          Education Qualification
        </h3>
      </div>
      <div class="grid grid-cols-12 gap-2">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
            >School/University</label
          >
          <input
            type="text"
            name="first-name"
            id="first-name"
            placeholder="School/University"
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
            >Qualification</label
          >
          <input
            type="text"
            name="last-name"
            id="last-name"
            placeholder="Qualification"
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
          <label
            for="date-of-birth"
            class="block text-sm font-medium text-gray-700"
            >Year of Passing</label
          >
          <input
            type="date"
            name="date-of-birth"
            placeholder="Company Mail"
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

        <div class="col-span-6 sm:col-span-2">
          <button
            type="button"
            @click="toggleModal"
            class="
              inline-flex
              mt-5
              justify-center
              py-2
              px-4
              border border-transparent
              shadow-sm
              text-sm
              font-medium
              rounded-md
              text-gray-600
              bg-white
              hover:bg-grey-700
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-500
            "
          >
            Add More
          </button>
        </div>
      </div>
      <div class="pt-4 pb-2">
        <h3 class="text-md leading-6 font-medium text-gray-900">
          Previous Work Experience
        </h3>
      </div>
      <div class="grid grid-cols-12 gap-2">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
            >Company Name
          </label>
          <input
            type="text"
            name="first-name"
            id="first-name"
            placeholder="Company Name"
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
            >Designation</label
          >
          <input
            type="text"
            name="last-name"
            id="last-name"
            placeholder="Designation"
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
        <div class="col-span-6 sm:col-span-2">
          <label
            for="blood-group"
            class="block text-sm font-medium text-gray-700"
            >Experience</label
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
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
            "
          >
            <option>Option 1</option>
            <option>Option 2</option>
          </select>
        </div>
        <div class="col-span-6 sm:col-span-2">
          <label
            for="date-of-birth"
            class="block text-sm font-medium text-gray-700"
            >Salary</label
          >
          <input
            type="date"
            name="date-of-birth"
            placeholder="Salary"
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

        <div class="col-span-6 sm:col-span-2">
          <button
            type="button"
            @click="toggleModal"
            class="
              inline-flex
              mt-5
              justify-center
              py-2
              px-4
              border border-transparent
              shadow-sm
              text-sm
              font-medium
              rounded-md
              text-gray-600
              bg-white
              hover:bg-grey-700
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-500
            "
          >
            Add More
          </button>
        </div>
      </div>
      <div class="pt-4 pb-2">
        <h3 class="text-md leading-6 font-medium text-gray-900">
          Credential Details
        </h3>
      </div>
      <div class="grid grid-cols-12 gap-2">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
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
          <label
            for="date-of-birth"
            class="block text-sm font-medium text-gray-700"
            >Passport No</label
          >
          <input
            type="date"
            name="date-of-birth"
            placeholder="Passport No"
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
            >License No</label
          >
          <input
            type="date"
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
            type="date"
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
            type="date"
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
            type="date"
            name="date-of-birth"
            placeholder="Salary"
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
      <div class="pt-4 pb-2">
        <h3 class="text-md leading-6 font-medium text-gray-900">References</h3>
      </div>
      <div class="grid grid-cols-12 gap-2">
        <div class="col-span-6 sm:col-span-3">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
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

        <div class="col-span-6 sm:col-span-2">
          <label
            for="first-name"
            class="block text-sm font-medium text-gray-700"
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

        <div class="col-span-6 sm:col-span-2">
          <label for="last-name" class="block text-sm font-medium text-gray-700"
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
        <div class="col-span-6 sm:col-span-2">
          <button
            type="button"
            @click="toggleModal"
            class="
              inline-flex
              mt-5
              justify-center
              py-2
              px-4
              border border-transparent
              shadow-sm
              text-sm
              font-medium
              rounded-md
              text-gray-600
              bg-white
              hover:bg-grey-700
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-500
            "
          >
            Add More
          </button>
        </div>
      </div>
      <div class="px-4 py-3 bg-white text-right sm:px-6">
        <button
          type="submit"
          class="
            inline-flex
            justify-center
            py-2
            px-4
            border border-transparent
            shadow-sm
            text-sm
            font-medium
            rounded-md
            text-white
            bg-indigo-600
            hover:bg-indigo-700
            focus:outline-none
            focus:ring-2
            focus:ring-offset-2
            focus:ring-indigo-500
          "
        >
          Save
        </button>
      </div>
    </form>
    <Modal :toggleModal="toggleModal" v-if="showmodal" />
  </div>
</template>

<script>
import Modal from "~/components/Modal";

export default {
  name: "EmployeeForm",
  components: {
    Modal,
  },
  data() {
    return {
      showmodal: false,
    };
  },

  methods: {
    async toggleModal() {
      this.showmodal = !this.showmodal;
    },
  },
};
</script>