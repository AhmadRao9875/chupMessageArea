<template>
  <div class="upload-message-container">
    <div
      class="forward-inner w-100 py-4 py-md-2 py-sm-1 px-4 px-md-2 px-sm-1 bg-white rounded rounded-4 d-flex flex-column"
    >
      <div class="header d-flex">
        <div class="crossSvg w-50">
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
        </div>

        <div
          class="forward-heading font-weight-bold d-flex w-50 justify-content-right"
        >
          <h2>Upload and Attach file</h2>
        </div>
      </div>

      <div
        class="inner d-flex flex-column align-items-center justify-content-center"
        v-show="showDiv"
      >
        <hr />
        <div class="file-note">
          <h4>Select or Drag file to upload</h4>
          <h6 class="text-gray">File size must be less then 20 MB</h6>
        </div>
        <button
          @click="uploadFile"
          class="btn for-canc green text-white font-weight-bold btn-lg"
        >
          Choose File
        </button>
        <!-- <input type="file" id="myFileInput" class="custom-file-input" />
        <label
          for="myFileInput"
          class="custom-file-label btn for-canc green text-white font-weight-bold btn-lg"
          >Choose File</label
        > -->

        <div class="downloading-file border-2 rounded">
          <div class="file-details">
            <div class="file">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                fill="currentColor"
                class="bi bi-file-earmark-arrow-up-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M9.293 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V4.707A1 1 0 0 0 13.707 4L10 .293A1 1 0 0 0 9.293 0zM9.5 3.5v-2l3 3h-2a1 1 0 0 1-1-1zM6.354 9.854a.5.5 0 0 1-.708-.708l2-2a.5.5 0 0 1 .708 0l2 2a.5.5 0 0 1-.708.708L8.5 8.707V12.5a.5.5 0 0 1-1 0V8.707L6.354 9.854z"
                />
              </svg>
            </div>
            <div class="name"><h5>this file is being uploaded</h5></div>
            <div class="crossSvg">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                fill="currentColor"
                class="bi bi-x"
                viewBox="0 0 16 16"
              >
                <path
                  d="M4.646 4.646a.5.5 0 0 1 .708 0L8 7.293l2.646-2.647a.5.5 0 0 1 .708.708L8.707 8l2.647 2.646a.5.5 0 0 1-.708.708L8 8.707l-2.646 2.647a.5.5 0 0 1-.708-.708L7.293 8 4.646 5.354a.5.5 0 0 1 0-.708z"
                />
              </svg>
            </div>
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
      showDiv: true,
    };
  },

  methods: {
    uploadFile() {
      this.$refs.fileInput.click();
    },
  },
};
</script>

<style>
.text-gray {
  color: #9d9d9d;
}

.custom-file-input {
  display: none; /* Hide the default file input button */
}

.custom-file-label {
  /* display: inline-block; */
  background-color: #125835;
  color: white;
  cursor: pointer;
}

.custom-file-label::after {
  background-color: #125835;
  content: ""; /* Remove default text */
}

.user-profile-pic {
  width: 50px;
  height: 50px;
  object-fit: cover;
  border-radius: 50%;
  position: relative;
  margin-right: 10px;
}
.downloading-file {
  border: 3px solid;
  border-color: #9d9d9d;
  border-radius: 1rem;
  width: 50%;
  max-height: 7rem;

}
.file-details {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  width: 100%;
height: 7rem;

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
