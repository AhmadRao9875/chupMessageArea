<template>
  <div class="nav-filter-container d-flex flex-column bg-light">
    <div
      class="nav-upper-bar w-100 d-flex justify-content-between py-md-3 py-sm-1 px-md-3 px-sm-1"
    >
      <div class="left-buttons d-flex flex-wrap">
        <ul class="nav nav-tabs mr-2">
          <a href="#" class="btn btn-outline-dark font-weight-bold">
            <i>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                fill="currentColor"
                class="bi bi-bar-chart-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M1 11a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v3a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1v-3zm5-4a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V7zm5-5a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v12a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V2z"
                />
              </svg>
            </i>
            General Analytics
          </a>
        </ul>

        <button class="btn btn-success text-white font-weight-bold">
          <i>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-bezier2"
              viewBox="0 0 16 16"
            >
              <path
                fill-rule="evenodd"
                d="M1 2.5A1.5 1.5 0 0 1 2.5 1h1A1.5 1.5 0 0 1 5 2.5h4.134a1 1 0 1 1 0 1h-2.01c.18.18.34.381.484.605.638.992.892 2.354.892 3.895 0 1.993.257 3.092.713 3.7.356.476.895.721 1.787.784A1.5 1.5 0 0 1 12.5 11h1a1.5 1.5 0 0 1 1.5 1.5v1a1.5 1.5 0 0 1-1.5 1.5h-1a1.5 1.5 0 0 1-1.5-1.5H6.866a1 1 0 1 1 0-1h1.711a2.839 2.839 0 0 1-.165-.2C7.743 11.407 7.5 10.007 7.5 8c0-1.46-.246-2.597-.733-3.355-.39-.605-.952-1-1.767-1.112A1.5 1.5 0 0 1 3.5 5h-1A1.5 1.5 0 0 1 1 3.5v-1zM2.5 2a.5.5 0 0 0-.5.5v1a.5.5 0 0 0 .5.5h1a.5.5 0 0 0 .5-.5v-1a.5.5 0 0 0-.5-.5h-1zm10 10a.5.5 0 0 0-.5.5v1a.5.5 0 0 0 .5.5h1a.5.5 0 0 0 .5-.5v-1a.5.5 0 0 0-.5-.5h-1z"
              />
            </svg>
          </i>
          User Journey
        </button>
      </div>
      <div class="right-buttons d-flex flex-wrap">
        <button
          class="btn btn-light rounded-0 btn-outline-dark font-weight-bold mr-2"
        >
          <i>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-filter"
              viewBox="0 0 16 16"
            >
              <path
                d="M6 10.5a.5.5 0 0 1 .5-.5h3a.5.5 0 0 1 0 1h-3a.5.5 0 0 1-.5-.5zm-2-3a.5.5 0 0 1 .5-.5h7a.5.5 0 0 1 0 1h-7a.5.5 0 0 1-.5-.5zm-2-3a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5z"
              />
            </svg>
          </i>
          Filter
        </button>
        <button
          class="btn btn-light rounded-0 btn-outline-dark font-weight-bold"
        >
          <i>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-cloud-arrow-down-fill"
              viewBox="0 0 16 16"
            >
              <path
                d="M8 2a5.53 5.53 0 0 0-3.594 1.342c-.766.66-1.321 1.52-1.464 2.383C1.266 6.095 0 7.555 0 9.318 0 11.366 1.708 13 3.781 13h8.906C14.502 13 16 11.57 16 9.773c0-1.636-1.242-2.969-2.834-3.194C12.923 3.999 10.69 2 8 2zm2.354 6.854-2 2a.5.5 0 0 1-.708 0l-2-2a.5.5 0 1 1 .708-.708L7.5 9.293V5.5a.5.5 0 0 1 1 0v3.793l1.146-1.147a.5.5 0 0 1 .708.708z"
              />
            </svg>
          </i>
          Export
        </button>
      </div>
    </div>
    <div
      class="nav-down-bar w-100 d-flex justify-content-between py-md-3 py-sm-1 px-md-3 px-sm-1 py-4 flex-wrap"
    >
      <div class="down-left-buttons w-5- d-flex justify-content-between flex-wrap">
        <button class="btn btn-success font-weight-bold text-white mr-2">
          <i>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-clock-fill"
              viewBox="0 0 16 16"
            >
              <path
                d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM8 3.5a.5.5 0 0 0-1 0V9a.5.5 0 0 0 .252.434l3.5 2a.5.5 0 0 0 .496-.868L8 8.71V3.5z"
              />
            </svg>
          </i>
          Live Queue
        </button>

        <!-- customized Slots modal -->

        <button
          class="btn font-weight-bold text-light-gray btn-outline-dark mr-2"
        >
          <i>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-calendar-minus"
              viewBox="0 0 16 16"
            >
              <path
                d="M5.5 9.5A.5.5 0 0 1 6 9h4a.5.5 0 0 1 0 1H6a.5.5 0 0 1-.5-.5z"
              />
              <path
                d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5zM1 4v10a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4H1z"
              />
            </svg>
          </i>
          Appointment
        </button>
        <li class="btn font-weight-bold text-light-gray btn-outline-dark mr-2">
          <a
            class="nav-link dropdown-toggle py-0 px-0 font-weight-bold"
            data-toggle="dropdown"
            href="#"
            role="button"
            aria-expanded="false"
            >Today</a
          >
          <div class="dropdown-menu">
            <a class="dropdown-item" href="#">Action</a>
            <a class="dropdown-item" href="#">Another action</a>
            <a class="dropdown-item" href="#">Something else here</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item" href="#">Separated link</a>
          </div>
        </li>
        <!-- <li
          class="btn nav-item dropdown font-weight-bold text-light-gray border-1 btn-outline-dark mr-2"
        >
          <a
            class="nav-link dropdown-toggle py-0 px-0"
            data-toggle="dropdown"
            href="#"
            role="button"
            aria-expanded="false"
            >Today</a
          >
          <div class="dropdown-menu">
            <a class="dropdown-item" href="#">Action</a>
            <a class="dropdown-item" href="#">Another action</a>
            <a class="dropdown-item" href="#">Something else here</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item" href="#">Separated link</a>
          </div>
        </li> -->
        <button
          class="btn font-weight-bold text-light-gray btn-outline-dark"
          data-toggle="modal"
          data-target="#filter"
        >
          Jan 13, 2023
        </button>
      </div>
      <div class="down-right-button">
        <button
          class="btn font-weight-bold text-dark btn-outline-dark"
          data-toggle="modal"
          data-target="#exampleModal"
        >
          Timeline
        </button>
      </div>
    </div>
    <!-- Customized Slots Modal -->
    <div
      class="modal fade"
      id="exampleModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable">
        <div class="modal-content">
          <div class="modal-header">
            <h3 class="modal-title" id="exampleModalLabel">
              Customized Available Slots
            </h3>
            <button
              type="button"
              class="close"
              data-dismiss="modal"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <div class="customizedSlots-inner">
              <div class="alert-text">
                <p class="text">
                  Enter the number of slots you would like to be available for
                  each LIVE QUEUE, WALK-INs and APPOINTMENTS,
                </p>
              </div>
              <hr />

              <div class="dropdown" @click="showOptions = !showOptions">
                <input
                  type="text"
                  class="form-control dropdown-toggle"
                  v-model="selectedOption"
                  placeholder="Select an option"
                />
                <svg
                  v-if="showSVG"
                  class="dropdown-icon"
                  viewBox="0 0 24 24"
                  style="width: 15px; height: 15px"
                >
                  <path
                    fill="currentColor"
                    d="M7.41,8.58L12,13.17l4.59-4.59c0.39-0.39,1.02-0.39,1.41,0l0,0c0.39,0.39,0.39,1.02,0,1.41l-5,5C12.01,15.39,11.74,15.5,11.5,15.5s-0.51-0.11-0.71-0.29l-5-5C6.97,9.6,6.97,8.97,7.41,8.58z"
                  ></path>
                </svg>
                <div
                  class="dropdown-menu"
                  :class="{ show: showOptions }"
                  aria-labelledby="dropdownMenuButton"
                >
                  <a
                    v-for="(option, index) in options"
                    :key="index"
                    class="dropdown-item"
                    href="#"
                    @click="selectOption(option)"
                  >
                    <img
                      :src="option.profilePic"
                      :alt="option.name"
                      class="profile-pic"
                    />
                    <span class="name">{{ option.name }}</span>
                  </a>
                </div>
              </div>
              <div class="day-year-dropdown">
                <div class="day-drop">
                  <select name="day" id="day" class="days">
                    <option value="" selected disabled>Day</option>
                    <option value="monday">Monday</option>
                    <option value="monda">Tuesday</option>
                    <option value="mond">Wednesday</option>
                    <option value="mon">Thursday</option>
                    <option value="mo">Friday</option>
                    <option value="m">Saturday</option>
                  </select>
                </div>
                <div class="year-drop"></div>
              </div>
              <hr />
              <div class="morning-slots">
                <div class="morning-title">
                  <h2>Morning's Slots</h2>
                </div>
                <div class="live-slots">
                  <div class="title">Live Queue Slots</div>
                  <div>
                    <input
                      type="number"
                      placeholder="0"
                      min="0"
                      v-model="liveSlots"
                      class="live-input live-input-width"
                    />
                  </div>
                </div>
                <div class="walkin-slots live-slots">
                  <div class="title">Live Queue Slots</div>
                  <div>
                    <input
                      type="number"
                      placeholder="0"
                      min="0"
                      v-model="liveSlots"
                      class="live-input live-input-width"
                    />
                  </div>
                </div>
                <div class="appointment-slots live-slots">
                  <div class="title">Live Queue Slots</div>
                  <div>
                    <input
                      type="number"
                      placeholder="0"
                      min="0"
                      v-model="liveSlots"
                      class="live-input live-input-width"
                    />
                  </div>
                </div>
              </div>
              <div class="morning-slots afternoon-slots">
                <div class="morning-title afternoon-title">
                  <h2>Afternoon's Slots</h2>
                </div>
                <div class="live-slots">
                  <div class="title">Live Queue Slots</div>
                  <div>
                    <input
                      type="number"
                      placeholder="0"
                      min="0"
                      v-model="liveSlots"
                      class="live-input live-input-width"
                    />
                  </div>
                </div>
                <div class="walkin-slots live-slots">
                  <div class="title">Live Queue Slots</div>
                  <div>
                    <input
                      type="number"
                      placeholder="0"
                      min="0"
                      v-model="liveSlots"
                      class="live-input live-input-width"
                    />
                  </div>
                </div>
                <div class="appointment-slots live-slots">
                  <div class="title">Live Queue Slots</div>
                  <div>
                    <input
                      type="number"
                      placeholder="0"
                      min="0"
                      v-model="liveSlots"
                      class="live-input live-input-width"
                    />
                  </div>
                </div>
              </div>
              <div class="clearall-sve-button">
                <button
                  class="clearall-button"
                  @click="clear"
                  data-dismiss="modal"
                >
                  Cear All
                </button>
                <button class="sve-button" @click="move">Save</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Filters Modal -->
    <div
      class="modal fade"
      id="filter"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Filter</h5>
            <button
              type="button"
              class="close"
              data-dismiss="modal"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <div class="filter-container">
              <div class="positions">
                <div class="sub-head">
                  <h6>Patient Status</h6>
                </div>
                <div class="service-options">
                  <label>
                    <input type="checkbox" value="1" />
                    Joining Queue
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Waiting
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Removed
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Served
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Delayed
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Arrived
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Option 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Serving
                  </label>
                </div>
              </div>

              <div class="service">
                <div class="sub-head pt-4">
                  <h6>Service</h6>
                </div>
                <div class="service-options">
                  <label>
                    <input type="checkbox" value="1" />
                    pediatrician
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Pharmacy
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Service 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Service 3
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Orthopedic
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Biling
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Service 2
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Service 4
                  </label>
                </div>
                <!-- <button class="showmore">show More</button> -->
              </div>

              <div class="service">
                <div class="sub-head pt-4">
                  <h6>Staff</h6>
                </div>
                <div class="service-options">
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                  <label>
                    <input type="checkbox" value="1" />
                    Doctor 1
                  </label>
                </div>
                <!-- <button class="showmore">show More</button> -->
              </div>
              <div class="waiting-time-slider pt-4">
                <div class="waiting-time-title">
                  <h6>Waiting Time: <span>1 hrs,14 min</span></h6>
                </div>
                <div id="time-slider" class="mt-4">
                  <div id="slider-handle"></div>
                  <div class="slider-track-waiting"></div>
                </div>
              </div>
              <div
                class="total-time-slider-containers d-flex justify-content between w-100"
              >
                <div class="total-queue pt-4 w-50">
                  <div class="waiting-time-title">
                    <h6>Total Time(Queue-End):</h6>
                    <span><p>1 hrs,14 min</p> </span>
                  </div>
                  <div id="time-slider" class="mt-4">
                    <div id="slider-handle"></div>
                    <div class="queue-time-track"></div>
                  </div>
                </div>
                <div class="total-arrive pt-4 w-50">
                  <div class="waiting-time-title">
                    <h6>Total Time(Arriving-End):</h6>
                    <span><p>1 hrs,14 min</p> </span>
                  </div>
                  <div id="time-slider" class="mt-4">
                    <div id="slider-handle"></div>
                    <div class="arive-time-track"></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="save-clear-buttons pt-3">
              <button class="save-button" @click="move">Apply</button>
              <button class="clear-button" data-dismiss="modal" @click="clear">
                Cear All
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "customizedSlots",
  data() {
    return {
      showOption: true,
      selectedOption: {},
      showOptions: false,
      showSVG: true,
      options: [
        { name: "John Doe", profilePic: "profile_pic_1.jpg" },
        { name: "Jane Smith", profilePic: "profile_pic_2.jpg" },
        { name: "Bob Johnson", profilePic: "profile_pic_3.jpg" },
        // Add more options here as needed
      ],
    };
  },
  mounted() {
    // Set the default option as the first option in the list
    console.log(this.selectOption);
    this.selectedOption = this.options[0].profilePic;
  },
  methods: {
    selectOption(option) {
      this.showSVG = false;
      this.selectedOption = option.name;
      this.showOptions = false;
      this.showSVG = true;
      // Do something with the selected option
    },
  },
};
</script>

<style>
.text-light-gray {
  color: #898d8f;
}
.btn-outline-dark {
  border-color: #898d8f;
}
a {
  color: #898d8f;
}

.nav-down-bar .btn.btn-success , .nav-upper-bar .btn.btn-success{
  background-color: #145635;
} 
.nav-down-bar {
  border: 2px solid #eeeff0;
  border-radius: 1rem;
  background-color: white;
}
.btn:hover {
  background-color: #fff;
  color: #898d8f;
  border-color: #343a40;
}

/* Customized Slots Style */
h1,
h2,
h3,
h4,
h5,
h6,
p,
li,
ul {
  margin: 0;
  padding: 0;
}
hr {
  width: 99%;
}

hr.line-break {
  border: none;
  border-top: 2px dotted blue;
  color: blue;
  /* background-color: blue; */
  height: 2px;
  margin: 0;
}

.title-svg {
  display: flex;
  width: 100%;
  align-items: center;
}
.title-box {
  width: 50%;
  padding-bottom: 1rem;
}

.svg {
  padding-left: 1rem;
  width: 50%;
  justify-content: end;
  display: flex;
}

.text {
  color: gray;
}
.dropdown {
  position: relative;
  margin-top: 1rem;
}
.dropdown-item {
  display: flex;
  align-items: center;
}

.dropdown-icon {
  position: absolute;
  right: 10%;
  top: 50%;
  transform: translateY(-50%);
  fill: #333;
  pointer-events: none;
}

.profile-pic {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  margin-right: 10px;
}

.name {
  font-weight: bold;
}
.dropdown-menu {
  display: none;
}
.show {
  display: block;
}
input {
}

select option:disabled {
  color: gray;
}

.day-drop {
  padding-top: 1rem;
}
.days {
  width: 7rem;
  height: 2rem;
  border-radius: 0.2rem;
}
.morning-slots {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
.afternoon-slots {
  padding-bottom: 1rem;
}
.live-slots {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background-color: rgb(217, 213, 213);
  border: transparent;
  border-radius: 0.5rem;
  height: 3rem;
}
.title {
  padding-left: 0.5rem;
}
.morning-title {
  padding-top: 1rem;
}
.live-input {
  background: transparent;
  height: 2rem;
  max-width: 10rem;
  text-align: center;
  border: 2px solid orangered;
  border-radius: 0.5rem;
  border-color: orangered;
}
.live-input-width {
  width: 90%;
}

.live-input ::placeholder {
  color: orangered;
}
.clearall-sve-button {
  padding-top: 1rem;
  display: flex;
  justify-content: flex-end;
}
.clearall-button,
.sve-button {
  width: 8rem;
  height: 2rem;
  border-radius: 1rem;
  text-align: center;
}
.sve-button {
  background-color: rgb(229, 230, 229);
  color: rgb(136, 135, 135);
  font-weight: bold;
  border: none;
}
.clearall-button {
  background-color: white;
  border-color: rgb(199, 196, 196);
  border-radius: 1rem;
}

/* service Filter style */

.service-options label {
  display: block;
  width: 7rem;
}
.service-options label:first-child {
  width: 8rem;
}
.sub-head {
  padding-bottom: 1rem;
}
.positions {
  display: flex;
  flex-direction: column;
}

.customer-options {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.service-options {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
/* .showmore {
  border: none;
  font-weight: bold;
  background: transparent;
  text-decoration: underline;
} */

.save-clear-buttons {
  display: flex;
}
.clear-button,
.save-button {
  width: 8rem;
  height: 2rem;
  border-radius: 1rem;
  text-align: center;
}
.save-button {
  background-color: rgb(1, 60, 1);
  color: white;
  font-weight: bold;
}

/* slider */
#time-slider {
  width: 100%;
  background-color: #ddd;
  position: relative;
}

#slider-handle {
  width: 10px;
  height: 10px;
  background-color: #333;
  position: absolute;
  top: -4.5px;
  left: 0%;
  transform: translateX(-50%);
  border-radius: 50%;
}
.arive-time-track,
.queue-time-track {
  widows: 100%;
  height: 2px;
  background-color: #aaa;
  position: absolute;
  top: 0;
  left: 0;
  transform: translateY(-50%);
  width: 95%;
}
.slider-track-waiting {
  width: 50%;
  height: 2px;
  background-color: #aaa;
  position: absolute;
  top: 0;
  left: 0;
  transform: translateY(-50%);
}
</style>
