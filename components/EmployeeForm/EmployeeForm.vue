 <template>
  <div class="mt-5 md:mt-0 md:col-span-2 py-4">
    <nav aria-label="Progress">
      <ol role="list" class="overflow-hidden">
        <li class="relative pb-5">
          <div
            class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full"
            :class="currentStep >= 1 ? 'bg-indigo-600' : 'bg-gray-300'"
            aria-hidden="true"
          ></div>

          <!-- Complete Step -->
          <a
            @click="jumbToStep(1)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center">
              <span
                v-if="currentStep > 1"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-indigo-600
                  rounded-full
                  group-hover:bg-indigo-800
                "
              >
                <!-- Heroicon name: solid/check -->
                <svg
                  class="w-5 h-5 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              <span
                v-if="currentStep <= 1"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2 border-indigo-600
                  rounded-full
                "
              >
                <span class="h-2.5 w-2.5 bg-indigo-600 rounded-full"></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="text-xs font-semibold tracking-wide uppercase"
                :class="currentStep == 1 ? 'text-indigo-600' : 'text-gray-500'"
                >General Details</span
              >
              <span class="text-sm text-gray-500"
                >Vitae sed mi luctus laoreet.</span
              >
            </span>
          </a>
          <div class="ml-8">
            <General v-if="currentStep == 1" :nextStep="nextStep" />
          </div>
        </li>

        <li class="relative pb-5">
          <div
            class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full"
            :class="currentStep >= 2 ? 'bg-indigo-600' : 'bg-gray-300'"
            aria-hidden="true"
          ></div>

          <!-- Complete Step -->
          <a
            @click="jumbToStep(2)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center">
              <span
                v-if="currentStep > 2"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  rounded-full
                "
                :class="
                  currentStep >= 2
                    ? 'bg-indigo-600 group-hover:bg-indigo-800'
                    : 'bg-gray-300 group-hover:bg-gray-400'
                "
              >
                <!-- Heroicon name: solid/check -->
                <svg
                  class="w-5 h-5 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              <span
                v-if="currentStep <= 2"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2
                  rounded-full
                "
                :class="
                  currentStep >= 2 ? 'border-indigo-600' : 'border-gray-300'
                "
              >
                <span
                  class="h-2.5 w-2.5 rounded-full"
                  :class="currentStep >= 2 ? 'bg-indigo-600' : 'bg-gray-300'"
                ></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="text-xs font-semibold tracking-wide uppercase"
                :class="currentStep == 2 ? 'text-indigo-600' : 'text-gray-500'"
                >Contact Details</span
              >
              <span class="text-sm text-gray-500"
                >Vitae sed mi luctus laoreet.</span
              >
            </span>
          </a>
          <div class="ml-8">
            <Contact
              v-if="currentStep == 2"
              :nextStep="nextStep"
              :goBack="goBack"
            />
          </div>
        </li>

        <li class="relative pb-5">
          <div
            class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full"
            :class="currentStep >= 3 ? 'bg-indigo-600' : 'bg-gray-300'"
            aria-hidden="true"
          ></div>

          <!-- Complete Step -->
          <a
            @click="jumbToStep(3)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center">
              <span
                v-if="currentStep > 3"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  rounded-full
                "
                :class="
                  currentStep >= 3
                    ? 'bg-indigo-600 group-hover:bg-indigo-800'
                    : 'bg-gray-300 group-hover:bg-gray-400'
                "
              >
                <!-- Heroicon name: solid/check -->
                <svg
                  class="w-5 h-5 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              <span
                v-if="currentStep <= 3"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2
                  rounded-full
                "
                :class="
                  currentStep >= 3 ? 'border-indigo-600' : 'border-gray-300'
                "
              >
                <span
                  class="h-2.5 w-2.5 rounded-full"
                  :class="currentStep >= 3 ? 'bg-indigo-600' : 'bg-gray-300'"
                ></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="text-xs font-semibold tracking-wide uppercase"
                :class="currentStep == 3 ? 'text-indigo-600' : 'text-gray-500'"
                >Employment Details</span
              >
              <span class="text-sm text-gray-500"
                >Vitae sed mi luctus laoreet.</span
              >
            </span>
          </a>
          <div class="ml-8">
            <Employment
              v-if="currentStep == 3"
              :nextStep="nextStep"
              :goBack="goBack"
            />
          </div>
        </li>
        <li class="relative pb-5">
          <div
            class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full"
            :class="currentStep >= 4 ? 'bg-indigo-600' : 'bg-gray-300'"
            aria-hidden="true"
          ></div>

          <!-- Complete Step -->
          <a
            @click="jumbToStep(4)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center">
              <span
                v-if="currentStep > 4"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  rounded-full
                "
                :class="
                  currentStep >= 4
                    ? 'bg-indigo-600 group-hover:bg-indigo-800'
                    : 'bg-gray-300 group-hover:bg-gray-400'
                "
              >
                <!-- Heroicon name: solid/check -->
                <svg
                  class="w-5 h-5 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              <span
                v-if="currentStep <= 4"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2
                  rounded-full
                "
                :class="
                  currentStep >= 4 ? 'border-indigo-600' : 'border-gray-300'
                "
              >
                <span
                  class="h-2.5 w-2.5 rounded-full"
                  :class="currentStep >= 4 ? 'bg-indigo-600' : 'bg-gray-300'"
                ></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="text-xs font-semibold tracking-wide uppercase"
                :class="currentStep == 4 ? 'text-indigo-600' : 'text-gray-500'"
              >
                Education Qualification</span
              >
              <span class="text-sm text-gray-500"
                >Vitae sed mi luctus laoreet.</span
              >
            </span>
          </a>
          <div class="ml-8">
            <Education
              v-if="currentStep == 4"
              :nextStep="nextStep"
              :goBack="goBack"
            />
          </div>
        </li>
        <li class="relative pb-5">
          <div
            class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full"
            :class="currentStep >= 5 ? 'bg-indigo-600' : 'bg-gray-300'"
            aria-hidden="true"
          ></div>

          <!-- Complete Step -->
          <a
            @click="jumbToStep(5)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center">
              <span
                v-if="currentStep > 5"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  rounded-full
                "
                :class="
                  currentStep >= 5
                    ? 'bg-indigo-600 group-hover:bg-indigo-800'
                    : 'bg-gray-300 group-hover:bg-gray-400'
                "
              >
                <!-- Heroicon name: solid/check -->
                <svg
                  class="w-5 h-5 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              <span
                v-if="currentStep <= 5"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2
                  rounded-full
                "
                :class="
                  currentStep >= 5 ? 'border-indigo-600' : 'border-gray-300'
                "
              >
                <span
                  class="h-2.5 w-2.5 rounded-full"
                  :class="currentStep >= 5 ? 'bg-indigo-600' : 'bg-gray-300'"
                ></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="text-xs font-semibold tracking-wide uppercase"
                :class="currentStep == 5 ? 'text-indigo-600' : 'text-gray-500'"
              >
                Previous Work Experience</span
              >
              <span class="text-sm text-gray-500"
                >Vitae sed mi luctus laoreet.</span
              >
            </span>
          </a>
          <div class="ml-8">
            <Experience
              v-if="currentStep == 5"
              :nextStep="nextStep"
              :goBack="goBack"
            />
          </div>
        </li>
        <li class="relative pb-5">
          <div
            class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full"
            :class="currentStep >= 6 ? 'bg-indigo-600' : 'bg-gray-300'"
            aria-hidden="true"
          ></div>

          <!-- Complete Step -->
          <a
            @click="jumbToStep(6)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center">
              <span
                v-if="currentStep > 6"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  rounded-full
                "
                :class="
                  currentStep >= 6
                    ? 'bg-indigo-600 group-hover:bg-indigo-800'
                    : 'bg-gray-300 group-hover:bg-gray-400'
                "
              >
                <!-- Heroicon name: solid/check -->
                <svg
                  class="w-5 h-5 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              <span
                v-if="currentStep <= 6"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2
                  rounded-full
                "
                :class="
                  currentStep >= 6 ? 'border-indigo-600' : 'border-gray-300'
                "
              >
                <span
                  class="h-2.5 w-2.5 rounded-full"
                  :class="currentStep >= 6 ? 'bg-indigo-600' : 'bg-gray-300'"
                ></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="text-xs font-semibold tracking-wide uppercase"
                :class="currentStep == 6 ? 'text-indigo-600' : 'text-gray-500'"
              >
                Credential Details</span
              >
              <span class="text-sm text-gray-500"
                >Vitae sed mi luctus laoreet.</span
              >
            </span>
          </a>
          <div class="ml-8">
            <Credential
              v-if="currentStep == 6"
              :nextStep="nextStep"
              :goBack="goBack"
            />
          </div>
        </li>
        <li class="relative pb-5">
          <div
            class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full"
            :class="currentStep >= 7 ? 'bg-indigo-600' : 'bg-gray-300'"
            aria-hidden="true"
          ></div>

          <!-- Complete Step -->
          <a
            @click="jumbToStep(7)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center">
              <span
                v-if="currentStep > 7"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  rounded-full
                "
                :class="
                  currentStep >= 7
                    ? 'bg-indigo-600 group-hover:bg-indigo-800'
                    : 'bg-gray-300 group-hover:bg-gray-400'
                "
              >
                <!-- Heroicon name: solid/check -->
                <svg
                  class="w-5 h-5 text-white"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              <span
                v-if="currentStep <= 7"
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2
                  rounded-full
                "
                :class="
                  currentStep >= 7 ? 'border-indigo-600' : 'border-gray-300'
                "
              >
                <span
                  class="h-2.5 w-2.5 rounded-full"
                  :class="currentStep >= 7 ? 'bg-indigo-600' : 'bg-gray-300'"
                ></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="text-xs font-semibold tracking-wide uppercase"
                :class="currentStep == 7 ? 'text-indigo-600' : 'text-gray-500'"
              >
                References</span
              >
              <span class="text-sm text-gray-500"
                >Vitae sed mi luctus laoreet.</span
              >
            </span>
          </a>
          <div class="ml-8">
            <References
              v-if="currentStep == 7"
              :nextStep="nextStep"
              :goBack="goBack"
            />
          </div>
        </li>

        <li class="relative">
          <!-- Upcoming Step -->
          <a
            @click="jumbToStep(1)"
            class="relative cursor-pointer flex items-start group"
          >
            <span class="h-9 flex items-center" aria-hidden="true">
              <span
                class="
                  relative
                  z-10
                  w-8
                  h-8
                  flex
                  items-center
                  justify-center
                  bg-white
                  border-2 border-gray-300
                  rounded-full
                  group-hover:border-gray-400
                "
              >
                <span
                  class="
                    h-2.5
                    w-2.5
                    bg-transparent
                    rounded-full
                    group-hover:bg-gray-300
                  "
                ></span>
              </span>
            </span>
            <span class="ml-4 min-w-0 flex flex-col">
              <span
                class="
                  text-xs
                  font-semibold
                  tracking-wide
                  uppercase
                  text-gray-500
                "
                >Preview</span
              >
              <span class="text-sm text-gray-500"
                >Iusto et officia maiores porro ad non quas.</span
              >
            </span>
          </a>
        </li>
      </ol>
    </nav>

    <Modal :toggleModal="toggleModal" v-if="showmodal" />
  </div>
</template>

<script>
import Modal from "~/components/Modal";
import General from "~/components/EmployeeForm/General.vue";
import Employment from "~/components/EmployeeForm/Employment.vue";
import Contact from "~/components/EmployeeForm/Contact.vue";
import Education from "~/components/EmployeeForm/Education.vue";
import Experience from "~/components/EmployeeForm/Experience.vue";
import Credential from "~/components/EmployeeForm/Credential.vue";
import References from "~/components/EmployeeForm/References.vue";

export default {
  name: "EmployeeForm",
  components: {
    Modal,
    General,
    Contact,
    Employment,
    Experience,
    Education,
    Credential,
    References,
  },
  data() {
    return {
      showmodal: false,
      currentStep: 1,
    };
  },

  methods: {
    async toggleModal() {
      this.showmodal = !this.showmodal;
    },
    async nextStep() {
      this.currentStep = this.currentStep + 1;
    },
    async goBack() {
      this.currentStep = this.currentStep - 1;
    },
    async jumbToStep(id) {
      this.currentStep = id;
    },
  },
};
</script>