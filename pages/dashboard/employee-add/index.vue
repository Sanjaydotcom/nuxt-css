<template>
  <div class="container mx-auto py-2">
    <div class="md:flex md:items-center md:justify-between md:space-x-5">
      <div class="flex items-start space-x-5">
        <div class="flex-shrink-0">
          <div class="relative mt-2">
            <img
              class="h-12 w-12 rounded-full"
              src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
              alt=""
            />
            <span
              class="absolute inset-0 shadow-inner rounded-full"
              aria-hidden="true"
            ></span>
          </div>
        </div>
        <!--
      Use vertical padding to simulate center alignment when both lines of text are one line,
      but preserve the same layout if the text wraps without making the image jump around.
    -->
        <div class="pt-1.5">
          <h1 class="text-2xl font-medium text-gray-600">Ricardo Cooper</h1>
          <p class="text-sm font-normal text-gray-500">EMP1234</p>
        </div>
      </div>
      <div
        class="
          mt-6
          flex flex-col-reverse
          justify-stretch
          space-y-4 space-y-reverse
          sm:flex-row-reverse
          sm:justify-end
          sm:space-x-reverse
          sm:space-y-0
          sm:space-x-3
          md:mt-0 md:flex-row md:space-x-3
        "
      >
        <button
          type="button"
          @click="toggleModal"
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
            focus:ring-indigo-400
          "
        >
          <!-- Heroicon name: solid/pencil -->

          Add Attachment
          <svg
            class="ml-1 mr-2 h-4 w-4"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            aria-hidden="true"
          >
            <path
              fill-rule="evenodd"
              d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z"
              clip-rule="evenodd"
            />
          </svg>
        </button>

        <select
          v-model="selectAction"
          @change="changeStatus"
          id="country"
          name="Gender"
          autocomplete="country-name"
          class="
            border border-gray-300
            bg-white
            rounded-md
            shadow-sm
            focus:outline-none focus:ring-indigo-400 focus:border-indigo-400
            sm:text-sm
            leading-4
            font-medium
            rounded-md
            text-gray-700
          "
          style="border-width: 0.25px"
        >
          <option>Actions</option>
          <option>Appraisal</option>
          <option>Change Status</option>
          <option>Staff Exit</option>
        </select>
      </div>
    </div>
    <div class="pt-3">
      <div class="sm:hidden">
        <!-- Use an "onChange" listener to redirect the user to the selected tab URL. -->
        <select
          id="tabs"
          name="tabs"
          class="
            block
            w-full
            pl-3
            pr-10
            py-2
            text-base
            border-gray-300
            focus:outline-none focus:ring-indigo-400 focus:border-indigo-400
            sm:text-sm
            rounded-md
          "
        >
          <option>General Details</option>

          <option>Asset</option>

          <option selected>Team Members</option>

          <option>Billing</option>
        </select>
      </div>
      <div class="hidden sm:block">
        <div class="border-b border-gray-200">
          <nav class="-mb-px flex space-x-8" aria-label="Tabs">
            <!-- Current: "border-indigo-400 text-indigo-600", Default: "border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300" -->
            <a
              href="#"
              class="
                border-transparent
                text-gray-700
                hover:text-gray-700 hover:border-gray-300
                whitespace-nowrap
                py-4
                px-1
                border-b-2
                font-medium
                text-sm
              "
              :class="visibleTabName == 'general' ? 'border-indigo-400' : ''"
              @click="openTab('general')"
            >
              General Details
            </a>

            <a
              href="#"
              class="
                border-transparent
                text-gray-700
                hover:text-gray-700 hover:border-gray-300
                whitespace-nowrap
                py-4
                px-1
                border-b-2
                font-medium
                text-sm
              "
              :class="visibleTabName == 'assets' ? 'border-indigo-400' : ''"
              @click="openTab('assets')"
            >
              Assets
            </a>

            <a
              href="#"
              class="
                border-transparent
                text-gray-700
                hover:text-gray-700 hover:border-gray-300
                whitespace-nowrap
                py-4
                px-1
                border-b-2
                font-medium
                text-sm
              "
              :class="visibleTabName == 'appraisal' ? 'border-indigo-400' : ''"
              @click="openTab('appraisal')"
            >
              Appraisal
            </a>
          </nav>
        </div>
      </div>

      <EmployeeForm v-if="visibleTabName == 'general'" />
      <Appraisal v-if="visibleTabName == 'appraisal'" />
      <Assets v-if="visibleTabName == 'assets'" />
    </div>
    <AddAttachment :toggleModal="toggleModal" v-if="addAttachmentModal" />
    <ChangeStatusModal
      :toggleModal="toggleChangeStausModal"
      v-if="changeStatusModal"
    />
    <StaffExitModal :toggleModal="toggleStaffExitModal" v-if="staffExitModal" />
  </div>
</template>

<script>
import PageHeader from "~/components/PageHeader";
import Employees from "~/components/Employees";
import EmployeeForm from "~/components/EmployeeForm/EmployeeForm.vue";
import AddAttachment from "~/components/AddAttachment.vue";
import ChangeStatusModal from "~/components/ChangeStatusModal.vue";
import StaffExitModal from "~/components/StaffExitModal.vue";

export default {
  name: "Employee-add",
  layout: "app",
  components: {
    PageHeader,
    Employees,
    EmployeeForm,
    AddAttachment,
    StaffExitModal,
    ChangeStatusModal,
  },
  data() {
    return {
      visibleTabName: "general",
      addAttachmentModal: false,
      changeStatusModal: false,
      selectAction: "Actions",
      staffExitModal: false,
    };
  },

  methods: {
    async toggleModal() {
      this.addAttachmentModal = !this.addAttachmentModal;
    },
    async toggleChangeStausModal() {
      this.changeStatusModal = !this.changeStatusModal;
    },
    async toggleStaffExitModal() {
      this.staffExitModal = !this.staffExitModal;
    },
    async changeStatus() {
      if (this.selectAction === "Change Status") {
        this.changeStatusModal = true;
      } else if (this.selectAction === "Staff Exit") {
        this.staffExitModal = true;
      }
    },

    openTab(tabName) {
      this.visibleTabName = tabName;
    },
  },
};
</script>
