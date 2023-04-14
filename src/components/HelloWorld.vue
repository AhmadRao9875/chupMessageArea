<template>
  <div class="message-container">
    <div class="message-wrapper">
      <div class="message-inner d-flex flex-wrap">
        <div class="chat-bar d-flex flex-column bg-white">
          <div class="profile-banner profile-banner-res d-flex flex-row py-3">
            <div class="profile-pic">
              <img src="../assets/icons8-user-80.png" alt="" />
            </div>
            <div class="profile-detail d-flex flex-column">
              <div class="profile-name mr-1 text-dark font-weight-bold">
                Drg.Maria Aurora T.,SPKGA
              </div>
              <div class="profile-status d-flex flex-row align-items-center">
                <div class="open btn text-center">Open</div>
                <div class="profession text-dark pl-1">Cardialogy</div>
              </div>
            </div>
          </div>
          <hr class="left-rule" />
          <div
            class="chats-feature d-flex flex-row justify-content-between align-items-center"
          >
            <div class="chats">Chats</div>
            <div
              class="feature d-flex flex-row justify-content-around border border-2 px-2 py-sm-1 mx-2 mx-md-2 mx-sm-1 px-sm-1 rounded"
            >
              <button
                class="btn btn-lg btn-white d-flex flex-column align-items-center feature-buttons"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-star-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
                    />
                  </svg>
                </i>

                Star
              </button>
              <button
                class="btn btn-lg btn-white d-flex flex-column align-items-center feature-buttons"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-archive-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M12.643 15C13.979 15 15 13.845 15 12.5V5H1v7.5C1 13.845 2.021 15 3.357 15h9.286zM5.5 7h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1 0-1zM.8 1a.8.8 0 0 0-.8.8V3a.8.8 0 0 0 .8.8h14.4A.8.8 0 0 0 16 3V1.8a.8.8 0 0 0-.8-.8H.8z"
                    />
                  </svg>
                </i>

                Archieve
              </button>
              <button
                class="btn btn-lg btn-white d-flex flex-column align-items-center feature-buttons"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-chat-left-text"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M14 1a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H4.414A2 2 0 0 0 3 11.586l-2 2V2a1 1 0 0 1 1-1h12zM2 0a2 2 0 0 0-2 2v12.793a.5.5 0 0 0 .854.353l2.853-2.853A1 1 0 0 1 4.414 12H14a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2H2z"
                    />
                    <path
                      d="M3 3.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zM3 6a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9A.5.5 0 0 1 3 6zm0 2.5a.5.5 0 0 1 .5-.5h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1-.5-.5z"
                    />
                  </svg>
                </i>

                Unread
              </button>
            </div>
          </div>
          <div
            class="search-bar w-100 d-flex align-items-center justify-content-center py-lg-2 py-md-1 py-sm-0"
          >
            <form class="form-inline my-2 my-lg-0">
              <input
                class="form-control search-holder width-80 mr-0"
                type="search"
                placeholder="Search"
                aria-label="Search"
              />
              <button
                class="btn btn-search bg-light my-2 my-sm-0"
                type="submit"
              >
                Search
              </button>
            </form>
          </div>
          <hr class="left-rule" />
          <div
            class="message-filters d-flex flex-wrap justify-content-between my-3 my-sm-2"
          >
            <a
              @click="showActiveMessage('all')"
              class="feature-btns nav-link pl-lg-4 pl-md-2 pl-sm-1 font-weight-bold"
              :class="{ active: activeTab === 'all' }"
            >
              All
            </a>
            <a
              @click="showActiveMessage('team')"
              class="feature-btns nav-link font-weight-bold"
              :class="{ active: activeTab === 'team' }"
            >
              Team
            </a>
            <a
              @click="showActiveMessage('pending')"
              class="feature-btns nav-link pending-color font-weight-bold d-flex align-items-center"
              :class="{ active: activeTab === 'pending' }"
            >
              Pending
              <i>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  fill="#E3672D"
                  class="bi bi-1-circle-fill ml-1"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0ZM9.283 4.002H7.971L6.072 5.385v1.271l1.834-1.318h.065V12h1.312V4.002Z"
                  />
                </svg>
              </i>
            </a>
          </div>
          <div
            v-show="activeTab === 'all'"
            class="message-box d-flex flex-column"
          ></div>
          <div
            v-show="activeTab === 'team'"
            class="message-box d-flex flex-column"
          >
            <div class="inbox-messages">
              <div
                @mouseover="changeBackgroundColor"
                :style="{ backgroundColor: first }"
                class="profile-banner d-flex flex-row py-lg-3 py-md-2 py-sm-1"
              >
                <div class="profile-pic">
                  <img src="../assets/icons8-user-80.png" alt="" />
                </div>
                <div class="profile-detail d-flex flex-column">
                  <div
                    class="profile-name mr-lg-2 mr-md-1 text-dark font-weight-bold d-flex py-3 py-sm-1 py-md-2 pl-2 align-items-center justify-content-between"
                  >
                    <div class="dr-name">Dr.LEE Kim En</div>
                    <div class="status text-gray ml-1 ml-sm-1 ml-md-2">
                      Offline
                    </div>
                    <div class="last-time ml-4 ml-md-2 ml-sm-1 text-gray">
                      00:41
                    </div>
                  </div>
                  <div class="last-message ml-4 ml-md-2 ml-sm-1">
                    <p>it's a dull pain and it feels like there's</p>
                  </div>
                </div>
              </div>
              <div
                @mouseover="changeBackgroundColor"
                class="profile-banner d-flex flex-row py-lg-3 py-md-2 py-sm-1"
                :style="{ backgroundColor: 'first' }"
              >
                <div class="profile-pic">
                  <img src="../assets/icons8-user-80.png" alt="" />
                </div>
                <div class="profile-detail d-flex flex-column">
                  <div
                    class="profile-name mr-lg-2 mr-md-1 text-dark font-weight-bold d-flex py-3 py-sm-1 py-md-2 pl-2 align-items-center justify-content-between"
                  >
                    <div class="dr-name">Dr.LEE Kim En</div>
                    <div class="status text-success ml-1 ml-sm-1 ml-md-2">
                      Online
                    </div>
                    <div class="last-time ml-4 ml-md-2 ml-sm-1 text-gray">
                      00:41
                    </div>
                  </div>
                  <div class="last-message ml-4 ml-md-2 ml-sm-1">
                    <p>it's a dull pain and it feels like there's</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div
            v-show="activeTab === 'pending'"
            class="message-box d-flex flex-column"
          >
            <div class="inbox-messages">
              <div
                class="profile-banner d-flex flex-row py-lg-3 py-md-2 py-sm-1 bg-white"
              >
                <div class="profile-pic">
                  <img src="../assets/icons8-user-80.png" alt="" />
                </div>
                <div class="profile-detail d-flex flex-column">
                  <div
                    class="profile-name mr-lg-2 mr-md-1 text-dark font-weight-bold d-flex py-3 py-sm-1 py-md-2 pl-2 align-items-center justify-content-between"
                  >
                    <div class="dr-name">Dr.LEE Kim En</div>
                    <div class="status text-gray ml-1 ml-sm-1 ml-md-2">
                      Offline
                    </div>
                    <div class="last-time ml-4 ml-md-2 ml-sm-1 text-gray">
                      00:41
                    </div>
                  </div>
                  <div class="last-message ml-4 ml-md-2 ml-sm-1">
                    <p>it's a dull pain and it feels like there's</p>
                  </div>
                </div>
              </div>
              <div
                class="profile-banner d-flex flex-row py-lg-3 py-md-2 py-sm-1 bg-message"
              >
                <div class="profile-pic">
                  <img src="../assets/icons8-user-80.png" alt="" />
                </div>
                <div class="profile-detail d-flex flex-column">
                  <div
                    class="profile-name mr-lg-2 mr-md-1 text-dark font-weight-bold d-flex py-3 py-sm-1 py-md-2 pl-2 align-items-center justify-content-between"
                  >
                    <div class="dr-name">Dr.LEE Kim En</div>
                    <div class="status text-success ml-1 ml-sm-1 ml-md-2">
                      Online
                    </div>
                    <div class="last-time ml-4 ml-md-2 ml-sm-1 text-gray">
                      00:41
                    </div>
                  </div>
                  <div class="last-message ml-4 ml-md-2 ml-sm-1">
                    <p>it's a dull pain and it feels like there's</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="chat-box d-flex flex-column bg-2nd-column-color align-items-center"
        >
          <div class="profile-names w-100">
            <div
              class="profiles align-items-center mr-auto py-4 py-md-2 py-sm-1 pl-3 pl-md-2 pl-sm-1 bg-white justify-content-start align-items-center ml-auto rounded d-flex"
            >
              <div class="images">
                <div class="image1">
                  <img src="../assets/icons8-user-80.png" alt="" />
                </div>
                <div class="image2">
                  <img src="../assets/icons8-user-80.png" alt="" />
                </div>
              </div>

              <div
                class="names mr-auto ml-4 ml-md-4 text-xl ml-sm-2 font-weight-bold font-600"
              >
                Dr Lee Kim En ,Saiful Jamal
              </div>
            </div>
          </div>
          <div class="note my-4 my-md-3 my-sm-1 py-2 py-md-1 py-sm-1">
            <div
              class="d-flex align-items-center justify-content-between px-4 px-md-2 px-sm-1 py-2 py-md-1 py-sm-1"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="25"
                height="25"
                fill="#FBB71E"
                class="bi bi-exclamation-circle-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM8 4a.905.905 0 0 0-.9.995l.35 3.507a.552.552 0 0 0 1.1 0l.35-3.507A.905.905 0 0 0 8 4zm.002 6a1 1 0 1 0 0 2 1 1 0 0 0 0-2z"
                />
              </svg>
              <h5 class="pl-2">
                <strong>Dr Lee Kim En</strong> You also check this message
                before sending it to the pataient
              </h5>
            </div>
          </div>
          <div class="date-time d-flex justify-content-start">
            <div class="date d-flex justify-content-center align-items-center">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="25"
                height="25"
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
              <h5 class="ml-3">wed, 22feb 2023</h5>
            </div>
            <div
              class="time d-flex justify-content-center align-items-center ml-5"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="25"
                height="25"
                fill="currentColor"
                class="bi bi-clock-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM8 3.5a.5.5 0 0 0-1 0V9a.5.5 0 0 0 .252.434l3.5 2a.5.5 0 0 0 .496-.868L8 8.71V3.5z"
                />
              </svg>
              <h5 class="ml-3">04:27:12 pm</h5>
            </div>
          </div>
          <div class="message mt-3">
            <textarea
              class="message-width font-weight-bold"
              name="message"
              id="message"
              rows="10"
            >
            
Lorem ipsum dolor sit, amet consectetur adipisicing elit. Impedit sapiente veniam praesentium nam quo amet tempora, nobis quidem inventore minima reiciendis? Ut accusantium voluptas deleniti dolor illum nulla provident accusamus.
            
            </textarea>
          </div>
          <div class="app-edit-send d-flex mt-3 mt-md-3 mt-sm-1">
            <button
              class="btn btn-all btn-green mr-3 text-white font-weight-bold"
            >
              Approve and send
            </button>
            <button class="btn btn-all mr-3 font-weight-bold">
              Edit Message
            </button>
            <button class="btn btn-all font-weight-bold">Reply Later</button>
          </div>
        </div>
        <div class="message-details d-flex flex-column bg-white">
          <div class="heading-name"><h5>About Saiful Jamal</h5></div>
          <div
            class="message-filters d-flex justify-content-between my-3 my-sm-2"
          >
            <a
              @click="showActiveFeature('details')"
              class="feature-btns feature-tag font-weight-bold"
              :class="{ active: activeFeature === 'details' }"
            >
              Details
            </a>
            <a
              @click="showActiveFeature('visits')"
              class="feature-btns feature-tag font-weight-bold"
              :class="{ active: activeFeature === 'visits' }"
              >Visits</a
            >
            <a
              @click="showActiveFeature('notes')"
              class="feature-btns feature-tag font-weight-bold d-flex align-items-center"
              :class="{ active: activeFeature === 'notes' }"
            >
              Notes
            </a>
            <a
              @click="showActiveFeature('files')"
              class="feature-btns feature-tag font-weight-bold"
              :class="{ active: activeFeature === 'files' }"
              >files</a
            >
          </div>
          <hr class="center-rule" />
          <div
            v-show="activeFeature === 'details'"
            class="feature-details w-100"
          >
            <div class="email-wht">
              <div class="email d-flex align-items-center mt-3">
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="30"
                    height="30"
                    fill="currentColor"
                    class="bi bi-envelope-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"
                    />
                  </svg>
                </i>
                <h6 class="ml-4 ml-md-2 ml-sm-1">khadijah123@gmail.com</h6>
              </div>
              <div class="whatsapp d-flex align-items-center mt-2 mb-3">
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="30"
                    height="30"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                </i>
                <h6 class="ml-4 ml-md-2 ml-sm-1">+0900 786 01</h6>
              </div>
            </div>
            <hr class="center-rule" />
            <div class="total-first">
              <div
                class="totla d-flex align-items-center justify-content-between mt-2"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-envelope-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"
                    />
                  </svg>
                  <span class="greyy-text ml-1">Total visits</span>
                </i>
                <h6 class="ml-4 ml-md-2 ml-sm-1">23</h6>
              </div>
              <div
                class="first-visit d-flex align-items-center justify-content-between mt-2 mb-2"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="greyy-text ml-1">First visit</span>
                </i>
                <div class="detail">
                  <button
                    @click="visitDetails('first')"
                    class="border-0 font-weight-bold bg-white"
                    name="detail"
                    id="detail"
                  >
                    23 Dec, 2023
                    <select
                      name=""
                      id=""
                      class="border-0 bg-white"
                      ref="dropdown"
                    ></select>
                  </button>
                </div>
              </div>
            </div>
            <div
              v-if="visit === 'first'"
              ref="firstVisit"
              class="details-box border mt-2 d-flex flex-column pr-2 pl-2"
            >
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Type</h5>
                <h6 class="black-text">Appointment</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Visit Status</h5>
                <h6 class="black-text">Served</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Time Started</h5>
                <h6 class="black-text">01:30</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Time Ended</h5>
                <h6 class="black-text">02:20</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Service</h5>
                <h6 class="black-text">Cardialogy</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Staff</h5>
                <h6 class="black-text">Dr. Le Kim En</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Reschedual</h5>
                <h6 class="black-text">3 times</h6>
              </div>
            </div>
            <div
              class="first-visit d-flex flex-column justify-content-between mt-4 mt-md-2 mt-md-1"
            >
              <div
                class="last-vist d-flex flex-row justify-content-between mt-4 mt-md-2 mt-md-1"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Last Visit</span
                  >
                </i>
                <button
                  @click="visitDetails('last')"
                  class="border-0 font-weight-bold bg-white"
                  name="detail"
                  id="detail"
                >
                  23 Dec, 2023
                  <select
                    name=""
                    id=""
                    class="border-0 bg-white"
                    ref="dropdown"
                  ></select>
                </button>
              </div>
              <div
                v-if="visit === 'last'"
                class="details-box border mt-2 d-flex flex-column pr-2 pl-2"
              >
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Type</h5>
                  <h6 class="black-text">Appointment</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Visit Status</h5>
                  <h6 class="black-text">Served</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Time Started</h5>
                  <h6 class="black-text">01:30</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Time Ended</h5>
                  <h6 class="black-text">02:20</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Service</h5>
                  <h6 class="black-text">Cardialogy</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Staff</h5>
                  <h6 class="black-text">Dr. Le Kim En</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Reschedual</h5>
                  <h6 class="black-text">3 times</h6>
                </div>
              </div>
              <div
                class="last-vist d-flex flex-row justify-content-between mt-4"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Current Vistit</span
                  >
                </i>
                <button
                  @click="visitDetails('current')"
                  class="border-0 font-weight-bold bg-white"
                  name="detail"
                  id="detail"
                >
                  23 Dec, 2023
                  <select
                    name=""
                    id=""
                    class="border-0 bg-white"
                    ref="dropdown"
                  ></select>
                </button>
              </div>
              <div
                v-if="visit === 'current'"
                class="details-box border mt-2 d-flex flex-column pr-2 pl-2"
              >
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Type</h5>
                  <h6 class="black-text">Appointment</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Visit Status</h5>
                  <h6 class="black-text">Served</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Time Started</h5>
                  <h6 class="black-text">01:30</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Time Ended</h5>
                  <h6 class="black-text">02:20</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Service</h5>
                  <h6 class="black-text">Cardialogy</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Staff</h5>
                  <h6 class="black-text">Dr. Le Kim En</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Reschedual</h5>
                  <h6 class="black-text">3 times</h6>
                </div>
              </div>
              <div
                class="last-vist d-flex flex-row justify-content-between mt-4"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Next Visit</span
                  >
                </i>
                <button
                  @click="visitDetails('next')"
                  class="border-0 font-weight-bold bg-white"
                  name="detail"
                  id="detail"
                >
                  23 Dec, 2023
                  <select
                    name=""
                    id=""
                    class="border-0 bg-white"
                    ref="dropdown"
                  ></select>
                </button>
              </div>
              <div
                v-if="visit === 'next'"
                class="details-box border mt-2 d-flex flex-column pr-2 pl-2"
              >
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Type</h5>
                  <h6 class="black-text">Appointment</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Visit Status</h5>
                  <h6 class="black-text">Served</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Time Started</h5>
                  <h6 class="black-text">01:30</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Time Ended</h5>
                  <h6 class="black-text">02:20</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Service</h5>
                  <h6 class="black-text">Cardialogy</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Staff</h5>
                  <h6 class="black-text">Dr. Le Kim En</h6>
                </div>
                <div
                  class="options d-flex align-items-center justify-content-between"
                >
                  <h5 class="greyy-text">Reschedual</h5>
                  <h6 class="black-text">3 times</h6>
                </div>
              </div>
            </div>
          </div>
          <div
            v-show="activeFeature === 'visits'"
            class="feature-details w-100"
          >
            <div class="total-first">
              <div
                class="totla d-flex align-items-center justify-content-between mt-2"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-envelope-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"
                    />
                  </svg>
                  <span class="greyy-text ml-1">Total visits</span>
                </i>
                <h6 class="ml-4 ml-md-2 ml-sm-1">23</h6>
              </div>
            </div>

            <div
              class="first-visit d-flex flex-column justify-content-between mt-4 mt-md-2 mt-md-1"
            >
              <div
                class="last-vist d-flex flex-row justify-content-between mt-4 mt-md-2 mt-md-1"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Last Visit</span
                  >
                </i>
                <div class="detail">
                  <select
                    class="border-0 font-weight-bold"
                    name="detail"
                    id="detail"
                  >
                    <option value="">23 Dec, 2023</option>
                  </select>
                </div>
              </div>

              <div
                class="last-vist d-flex flex-row justify-content-between mt-4"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Current Vistit</span
                  >
                </i>
                <div class="detail">
                  <select
                    class="border-0 font-weight-bold"
                    name="detail"
                    id="detail"
                  >
                    <option value="">In Queue</option>
                  </select>
                </div>
              </div>
              <div
                class="last-vist d-flex flex-row justify-content-between mt-4"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Next Visit</span
                  >
                </i>
                <div class="detail">
                  <select
                    class="border-0 font-weight-bold"
                    name="detail"
                    id="detail"
                  >
                    <option value="">23 Dec, 2023</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
          <div v-show="activeFeature === 'notes'" class="feature-details w-100">
            <div class="total-first">
              <div
                class="totla d-flex align-items-center justify-content-between mt-2"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-envelope-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"
                    />
                  </svg>
                  <span class="greyy-text ml-1">Total visits</span>
                </i>
                <h6 class="ml-4 ml-md-2 ml-sm-1">23</h6>
              </div>
            </div>
            <div class="details-box border mt-2 d-flex flex-column pr-2 pl-2">
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Type</h5>
                <h6 class="black-text">Appointment</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Visit Status</h5>
                <h6 class="black-text">Served</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Time Started</h5>
                <h6 class="black-text">01:30</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Time Ended</h5>
                <h6 class="black-text">02:20</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Service</h5>
                <h6 class="black-text">Cardialogy</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Staff</h5>
                <h6 class="black-text">Dr. Le Kim En</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Reschedual</h5>
                <h6 class="black-text">3 times</h6>
              </div>
            </div>
            <div
              class="first-visit d-flex flex-column justify-content-between mt-4 mt-md-2 mt-md-1"
            >
              <div
                class="last-vist d-flex flex-row justify-content-between mt-4 mt-md-2 mt-md-1"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Last Visit</span
                  >
                </i>
                <div class="detail">
                  <select
                    class="border-0 font-weight-bold"
                    name="detail"
                    id="detail"
                  >
                    <option value="">23 Dec, 2023</option>
                  </select>
                </div>
              </div>

              <div
                class="last-vist d-flex flex-row justify-content-between mt-4"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-whatsapp"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"
                    />
                  </svg>
                  <span class="font-weight-bold greyy-text ml-1"
                    >Next Visit</span
                  >
                </i>
                <div class="detail">
                  <select
                    class="border-0 font-weight-bold"
                    name="detail"
                    id="detail"
                  >
                    <option value="">23 Dec, 2023</option>
                  </select>
                </div>
              </div>
            </div>
          </div>
          <div v-show="activeFeature === 'files'" class="feature-details w-100">
            <div class="total-first">
              <div
                class="totla d-flex align-items-center justify-content-between mt-2"
              >
                <i>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="15"
                    height="15"
                    fill="currentColor"
                    class="bi bi-envelope-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"
                    />
                  </svg>
                  <span class="greyy-text ml-1">Total visits</span>
                </i>
                <h6 class="ml-4 ml-md-2 ml-sm-1">23</h6>
              </div>
            </div>
            <div class="details-box border mt-2 d-flex flex-column pr-2 pl-2">
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Type</h5>
                <h6 class="black-text">Appointment</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Visit Status</h5>
                <h6 class="black-text">Served</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Time Started</h5>
                <h6 class="black-text">01:30</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Time Ended</h5>
                <h6 class="black-text">02:20</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Service</h5>
                <h6 class="black-text">Cardialogy</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Staff</h5>
                <h6 class="black-text">Dr. Le Kim En</h6>
              </div>
              <div
                class="options d-flex align-items-center justify-content-between"
              >
                <h5 class="greyy-text">Reschedual</h5>
                <h6 class="black-text">3 times</h6>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      activeTab: "pending",
      activeFeature: "details",
      visit: null,
      first: "bg-white",
      second: "bg-message",
    };
  },
  methods: {
    showActiveMessage(tab) {
      console.log(tab);
      this.activeTab = tab;
    },
    showActiveFeature(feature) {
      this.activeFeature = feature;
    },
    visitDetails(details) {
      if (this.visit === details) {
        this.visit = null;
      } else {
        this.visit = details;
      }
    },
    changeBackgroundColor() {
      console.log("this is mousehover");
      if (this.first === "white") {
        this.first = "#f0f0f0";
      } else {
        this.first = "white";
      }
    },
  },
};
</script>

<style>
p,
h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0;
}
.message-inner {
  width: 100%;
}
.chat-bar {
  width: 30%;
}
.chat-box {
  width: 50%;
}
.message-details {
  width: 20%;
  height: auto;
}

.profile-pic img {
  border-radius: 50%;
  width: 4rem;
  height: 4rem;
  background-color: rgb(226, 222, 222);
}
.profile-name {
  font-size: 1rem;
}
.width-80 {
  width: 80%;
}
.open {
  background-color: #d0f8e7;
  border: 2px;
  border-radius: 2rem;
  width: 4rem;
  height: 1.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
.profession {
  font-size: 1.3rem;
}
.left-rule {
  border: none;
  height: 5px;
  background-color: #dedada;
  margin: 10px 0;
}
.center-rule {
  border: none;
  height: 1px;
  background-color: #dedada;
  margin: 2px 0;
}
.chats-feature {
  width: 100%;
}
.chats {
  width: 40%;
  font-size: 1rem;
  font-weight: bold;
}
.feature {
  max-height: 5rem;
}
.btn-lg {
  padding: 0;
  padding-right: 1rem;
}
.btn-lg:first-child {
  padding-left: 1rem;
  border-right: #a0a4a6;
}
.feature-buttons {
  /* position: relative; */
}
/* .feature button ::after {
  content: "";
  position: absolute;
  top: 50%;
  right: 10%; 
  transform: translateY(-50%);
  height: 70%; 
  width: 2px; 
  background-color: #d5d3d3; 
} */
.feature button::after:last-child {
  display: none;
}

.search-holder {
  border-right: none;
}
.btn-search {
  border-left: none;
  width: 4rem;
}
.message-filters {
  height: auto;
}
.text-gray {
  color: #6d6d6d;
}
.greyy-text {
  color: #6d6d6d;
  font-size: 0.8rem;
}
/* .pending-color {
  color: #e3672d;
} */
.black-text {
  color: black;
  font-size: 0.9rem;
  font-weight: bold;
}
.bg-message {
  background-color: #f0f0f0;
}
.bg-2nd-column-color {
  background-color: #f7f8fc;
}

/* center Column */

.profiles {
  width: 98%;
}
.image1 {
  position: absolute;
  top: 0;
  left: 20%;
}
.image2 {
  /* position: relative; */
}
.images {
  position: relative;
  max-width: 30%;
}
.images img {
  width: 1.5rem;
  height: 1.5rem;
  border-radius: 50%;
  border: 2px solid black;
}
.note {
  background-color: #fef2d3;
  max-width: 90%;
  border-radius: 1rem;
  border: 2px solid orange;
}
.date-time {
  width: 90%;
}

.message {
  width: 90%;
}

.message-width {
  width: 100%;
  border-radius: 0.5rem;
  border-top-left-radius: none;
}

.btn-all {
  max-width: 12rem;
  height: auto;
  border-radius: 2rem;
  border: 2px solid gray;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}
a {
  text-decoration: none;
}
.feature-btns {
  text-decoration: none;
  margin: 0;
  padding: 5px;
  cursor: pointer;
  color: #a0a4a6;
  /* border-bottom: 3px solid transparent; */
}
.feature-tag {
  text-decoration: none;
  cursor: pointer;
  color: #a0a4a6;
  border-bottom: 3px solid transparent;
}
.feature-tag.active {
  border-bottom-color: #d99d81;
  color: #d99d81;
}
.feature-tag:hover {
  text-decoration: none;
  color: #d99d81;
}

.btn-green {
  background-color: #125934;
}

.column {
  flex-basis: 100%;
}
/* a.active {
  color: #e3672d;
} */
.nav-link {
  text-decoration: none;
  cursor: pointer;
  color: #a0a4a6;

  border-bottom: 3px solid transparent; /* Add a transparent border to create space for the line */
}
.nav-link.active {
  border-bottom-color: #e3672d;
  color: #e3672d;
}

/* Media Query */
@media only screen and (max-width: 1200px) {
  .message-inner {
  }
  .chat-bar {
    width: 30%;
  }
  .chat-box {
    width: 40%;
  }
  .message-details {
    width: 30%;
    height: 100%;
    justify-content: center;
  }
  .message-filters {
    flex-wrap: wrap;
  }
  .chats-feature {
    flex-wrap: wrap;
  }
  .feature {
    margin: 0;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  .feature-buttons {
    margin: 10px;
    padding: 0;
    font-size: 1rem;
  }
  .search-holder {
    width: 70%;
  }
}
@media only screen and (max-width: 760px) {
  .form-inline .form-control {
    display: inline-block;
    width: 70%;
    vertical-align: middle;
  }
  .message-inner {
    flex-direction: column;
  }
  .chat-bar {
    width: 100%;
  }
  .chat-box {
    width: 100%;
  }
  .message-details {
    width: 100%;
    justify-content: center;
  }
  .profile-banner-res {
    justify-content: center;
    align-items: center;
  }
  .profile-detail {
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
  .chats-feature {
    justify-content: space-around !important;
  }
  .chats {
    width: 30%;
  }
  .feature {
    width: 60%;
  }
  .chat-box {
    padding-top: 2rem;
    padding-left: 2rem;
    padding-right: 2rem;
  }
  .profiles {
    width: 100%;
    height: auto;
  }
  .note {
    height: auto;

    max-width: 100%;
  }
  .message {
    width: 100% !important;
  }
  .app-edit-send {
    width: 100%;
    justify-content: space-around;
  }
  .greyy-text {
    font-size: 1rem;
  }
  .message-details {
    padding: 2rem;
    justify-content: center !important;
  }
}
@media only screen and (max-width: 500px) {
  .feature {
    padding: 1rem;
    margin: 0;
    width: 100%;
  }
  .chats-feature {
    flex-direction: column;
  }
  .chat-box {
    margin: 0;
    padding: 0;
    width: 100%;
  }
}
</style>
