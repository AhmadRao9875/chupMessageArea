<template>
  <div class="forward-message-container">
    <div
      class="forward-inner w-100 py-4 py-md-2 py-sm-1 px-4 px-md-2 px-sm-1 bg-white rounded rounded-4 d-flex flex-column"
    >
      <div class="cross">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="40"
          height="40"
          fill="currentColor"
          class="bi bi-x"
          viewBox="0 0 16 16"
          @click="showDiv = !showDiv"
        >
          <path
            d="M4.646 4.646a.5.5 0 0 1 .708 0L8 7.293l2.646-2.647a.5.5 0 0 1 .708.708L8.707 8l2.647 2.646a.5.5 0 0 1-.708.708L8 8.707l-2.646 2.647a.5.5 0 0 1-.708-.708L7.293 8 4.646 5.354a.5.5 0 0 1 0-.708z"
          />
        </svg>
        <div class="inner" v-show="showDiv">
          <div class="forward-heading font-weight-bold d-flex flex-column">
            <h2>Forward message to check</h2>
            <h5 class="text-gray">
              Send message to check by Admin/ Doctor , before sending to the
              patient
            </h5>
          </div>
          <hr />
          <form class="form-inline my-2 my-lg-0 w-100">
            <input
              class="form-control search-bar w-95"
              type="search"
              placeholder="Search Admin Doctor"
              aria-label="Search"
            />
            <button
              class="btn search-btn btn-outline-success my-2 my-sm-0 w-5"
              type="submit"
            >
              Search
            </button>
          </form>
          <div class="staff-list">
            <div v-for="user in staff" :key="user.id" class="user-container">
              <input
                type="checkbox"
                v-model="user.isSelected"
                @change="updateSelectedUsers"
              />
              <img
                class="user-profile-pic"
                :src="user.profile"
                alt="Profile Pic"
              />
              <div class="online-badge"></div>
              <span class="user-name">{{ user.name }}</span>
            </div>
          </div>
          <hr />
          <div class="forward-cancel d-flex">
            <button
              @click="showSelected"
              class="btn for-canc green text-white font-weight-bold btn-lg"
            >
              Forward
            </button>
            <button class="btn for-canc gray btn-lg">Cancel</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      staff: [
        {
          profile: require("@/assets/icons8-user-80.png"),
          name: "Dr.Lee Kim En",
          service: "sPoG",
        },
        {
          profile: require("@/assets/icons8-user-80.png"),
          name: "Dr.Lee Kim En",
          service: "sPoG",
        },
        {
          profile: require("@/assets/icons8-user-80.png"),
          name: "Dr.Lee Kim En",
          service: "sPoG",
        },
        {
          profile: require("@/assets/icons8-user-80.png"),
          name: "Dr.Lee Kim En",
          service: "sPoG",
        },
        {
          profile: require("@/assets/icons8-user-80.png"),
          name: "Dr.Lee Kim En",
          service: "sPoG",
        },
        {
          profile: require("@/assets/icons8-user-80.png"),
          name: "Dr.Lee Kim En",
          service: "sPoG",
        },
      ],
      selectedUser: [],
      showDiv: true,
    };
  },

  methods: {
    updateSelectedUsers() {
      console.log("selected");
      this.selectedUser = [];
      //   this.selectedUsers = this.staff.filter(user => user?.isSelected);
      for (let i = 0; i <= this.staff.length; i++) {
        if (this.staff[i] && this.staff[i].isSelected) {
          this.selectedUser.push(this.staff[i]);
        }
      }
      console.log("selected");
    },
    showSelected() {
      console.log("this is active");
      console.log(this.selectedUser);
      return this.selectedUser;
    },
  },
};
</script>

<style>
.text-gray {
  color: #9d9d9d;
}
.w-95 {
  width: 80%;
}
.w-5 {
  width: auto;
}
.search-btn {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
  border-left: none;
  border-color: transparent;
  background-color: #efefef;
}
.search-bar {
  /* border-right: none; */
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
.user-container {
  position: relative;
  /* display: inline-block; */
}
.user-profile-pic {
  width: 50px;
  height: 50px;
  object-fit: cover;
  border-radius: 50%;
  position: relative;
  margin-right: 10px;
}
.online-badge {
  position: absolute;
  width: 0.5rem;
  height: 0.5rem;
  top: 80%;
  left: 4%;
  border-radius: 50%;
  background-color: green;
  opacity: 0.8;
}

.user-name {
  font-weight: bold;
  margin-right: 10px;
}
.green {
  background-color: #125835;
}
.gray {
  color: #b9b9b9;
}
.for-canc {
  border-radius: 2rem;
  border: 2px solid;
  max-width: 10rem;
}
</style>
