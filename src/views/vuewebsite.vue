<template>
  <section>
    <div class="container-fluid p-0 m-auto">
      <div id="website-builder" class="d-flex mx-0 justify-content-between">
        <div class="p-0">
          <div class="d-flex position-sticky sticky-index align-items-start">
            <div
              class="maintabs position-relative nav flex-column nav-pills"
              id="v-pills-tab"
              role="tablist"
              aria-orientation="vertical"
            >
              <button
                @click="toggleMode('edit')"
                class="nav-link active"
                id="v-pills-home-tab"
                data-bs-toggle="pill"
                data-bs-target="#v-pills-home"
                type="button"
                role="tab"
                aria-controls="v-pills-home"
                aria-selected="true"
              >
                <img src="./assets/images/mode-plus-on.svg" alt="" />
              </button>
              <button
                @click="toggleMode('edit')"
                class="nav-link"
                id="v-pills-profile-tab"
                data-bs-toggle="pill"
                data-bs-target="#v-pills-profile"
                type="button"
                role="tab"
                aria-controls="v-pills-profile"
                aria-selected="false"
              >
                <img src="./assets/images/mode-drop.svg" alt="" />
              </button>
              <button
                @click="toggleMode('preview')"
                class="nav-link"
                id="v-pills-messages-tab"
                data-bs-toggle="pill"
                data-bs-target="#v-pills-messages"
                type="button"
                role="tab"
                aria-controls="v-pills-messages"
                aria-selected="false"
              >
                <img src="./assets/images/mode-list.svg" alt="" />
              </button>

              <button
                class="nav-link"
                id="v-pills-settings-tab"
                data-bs-toggle="pill"
                data-bs-target="#v-pills-settings"
                type="button"
                role="tab"
                aria-controls="v-pills-settings"
                aria-selected="false"
              >
                <img src="" alt="" />
              </button>
            </div>
            <div
              class="maintabscontent position-absolute tab-content"
              id="v-pills-tabContent"
            >
              <div
                class="tab-pane p-0 fade text-white show active"
                id="v-pills-home"
                role="tabpanel"
                aria-labelledby="v-pills-home-tab"
              >
                <div class="d-flex align-items-start">
                  <div
                    class="nav secontTabMain flex-column nav-pills"
                    id="v-pills-tab"
                    role="tablist"
                    aria-orientation="vertical"
                  >
                    <ul class="mb-0 list-unstyled nice-scroll">
                      <li data-group="navigations" class="active bold p-3">
                        <h4 class="text-secondary activaNavigate mb-0">Section</h4>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white text-start w-100"
                          id="v-pills-home-tab1"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-home1"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-home1"
                          aria-selected="true"
                        >
                          Layout Builder
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-profile-tab1"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-profile1"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-profile1"
                          aria-selected="false"
                        >
                          Cards
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-messages-tab1"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-messages1"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-messages1"
                          aria-selected="false"
                        >
                          Table
                        </button>
                      </li>
                    </ul>
                  </div>
                  <div class="tab-content secontTabContent" id="v-pills-tabContent">
                    <div
                      class="tab-pane p-2"
                      id="v-pills-home1"
                      role="tabpanel"
                      aria-labelledby="v-pills-home-tab1"
                    >
                      <ul class="list-unstyled nice-scroll">
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          Row
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          <div class="bg-light border rounded w-100 bgBlue p-3"></div>
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          <div class="d-flex">
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 ms-1"
                            ></div>
                          </div>
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          <div class="d-flex">
                            <div
                              class="w-30 bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 ms-1"
                            ></div>
                          </div>
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          <div class="d-flex">
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div
                              class="w-30 bg-light border rounded w-100 bgBlue p-3 ms-1"
                            ></div>
                          </div>
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          <div class="d-flex">
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div class="bg-light border rounded w-100 bgBlue p-3"></div>
                          </div>
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          <div class="d-flex">
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue p-3 me-1"
                            ></div>
                            <div class="bg-light border rounded w-100 bgBlue p-3"></div>
                          </div>
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li class="p-2 cursor-pointer position-relative moveScroll">
                          <div class="d-flex">
                            <div
                              class="bg-light border rounded w-100 bgBlue py-3 px-2 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue py-3 px-2 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue py-3 px-2 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue py-3 px-2 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue py-3 px-2 me-1"
                            ></div>
                            <div
                              class="bg-light border rounded w-100 bgBlue py-3 px-2"
                            ></div>
                          </div>
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane p-2 fade text-white"
                      id="v-pills-profile1"
                      role="tabpanel"
                      aria-labelledby="v-pills-profile1-tab1"
                    >
                      <ul class="list-unstyled nice-scroll">
                        <li
                          data-type="CardOne"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 rounded"
                            src="./assets/images/card1.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>

                        <li
                          data-type="CardTwo"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 rounded"
                            src="./assets/images/card2.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="CardThree"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 rounded"
                            src="./assets/images/card3.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="CardFour"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 rounded"
                            src="./assets/images/card4.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="CardFive"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 rounded"
                            src="./assets/images/card6.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="CardSix"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 rounded cardHeight"
                            src="./assets/images/card7.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane p-2 fade text-white"
                      id="v-pills-messages1"
                      role="tabpanel"
                      aria-labelledby="v-pills-messages-tab1"
                    >
                      <ul class="list-unstyled nice-scroll">
                        <li
                          data-type="ListOne"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 h-auto rounded cardHeight"
                            src="./assets/images/menu1.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="ListTwo"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 h-auto rounded cardHeight"
                            src="./assets/images/menu2.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="ListThree"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 h-auto rounded cardHeight"
                            src="./assets/images/menu3.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="ListFour"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 h-auto rounded cardHeight"
                            src="./assets/images/menu4.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="ListFive"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 h-auto rounded cardHeight"
                            src="./assets/images/menu5.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="ListSix"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 h-auto rounded cardHeight"
                            src="./assets/images/menu6.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                        <li
                          data-type="ListSeven"
                          draggable="true"
                          @dragstart="handleDragStart"
                          class="p-2 h-auto cursor-pointer position-relative moveScroll"
                        >
                          <img
                            class="w-100 h-auto rounded cardHeight"
                            src="./assets/images/menu7.png"
                            alt="..."
                          />
                          <div
                            class="w-100 h-100 position-absolute d-flex align-items-center justify-content-center add-section rounded"
                          >
                            <img src="./assets/images/plus.svg" alt="..." />
                          </div>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
              <div
                class="tab-pane fade text-white"
                id="v-pills-profile"
                role="tabpanel"
                aria-labelledby="v-pills-profile-tab"
              >
                <div class="d-flex align-items-start">
                  <div
                    class="nav secontTabMain flex-column nav-pills"
                    id="v-pills-tab"
                    role="tablist"
                    aria-orientation="vertical"
                  >
                    <ul class="mb-0 list-unstyled nice-scroll">
                      <li data-group="navigations" class="active bold p-3">
                        <h4 class="text-secondary activaNavigate mb-0">Global Style</h4>
                      </li>
                      <!-- <li>
                      <div class="btn-group d-flex mt-3" role="group" aria-label="...">
                        <button data-id="light" type="button"
                          class="supra-btn pb-2 btn-default w-50 bg-transparent border-0 text-white">
                          <span>Light</span></button><button data-id="dark" type="button"
                          class="supra-btn btn-default active w-50 bg-transparent border-0 text-white pb-2">
                          <span>Dark</span>
                        </button>
                      </div>
                    </li> -->
                      <li class="navLink">
                        <button
                          class="nav-link text-white text-start w-100"
                          id="v-pills-home-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-home2"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-home2"
                          aria-selected="true"
                        >
                          Body
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-profile-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-profile2"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-profile2"
                          aria-selected="false"
                        >
                          Sections
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-messages-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-messages2"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-messages2"
                          aria-selected="false"
                        >
                          H1
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-messagesh2-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-messagesh2"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-messagesh2"
                          aria-selected="false"
                        >
                          H2
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-messagesh3-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-messagesh3"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-messagesh3"
                          aria-selected="false"
                        >
                          H3
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-messagesh4-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-messagesh4"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-messagesh4"
                          aria-selected="false"
                        >
                          H4
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-link-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-link"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-link"
                          aria-selected="false"
                        >
                          links
                        </button>
                      </li>

                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-Buttons-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-Buttons"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-Buttons"
                          aria-selected="false"
                        >
                          Buttons
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-Buttonsprimary-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-Buttonsprimary"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-Buttonsprimary"
                          aria-selected="false"
                        >
                          Buttons Primary
                        </button>
                      </li>
                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-Buttonsecondary-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-Buttonsecondary"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-Buttonsecondary"
                          aria-selected="false"
                        >
                          Button Secondary
                        </button>
                      </li>

                      <li class="navLink">
                        <button
                          class="nav-link text-white w-100 text-start"
                          id="v-pills-Other-tab2"
                          data-bs-toggle="pill"
                          data-bs-target="#v-pills-Other"
                          type="button"
                          role="tab"
                          aria-controls="v-pills-Other"
                          aria-selected="false"
                        >
                          Other
                        </button>
                      </li>
                    </ul>
                  </div>
                  <div
                    class="tab-content show active fade secontTabContent"
                    id="v-pills-tabContent"
                  >
                    <div
                      class="tab-pane p-2"
                      id="v-pills-home2"
                      role="tabpanel"
                      aria-labelledby="v-pills-home-tab2"
                    >
                      <div>
                        <ul class="list-unstyled mb-0">
                          <li
                            data-group="navigations"
                            class="active bold p-2 d-flex justify-content-between"
                          >
                            <h4 class="text-secondary activaNavigate mb-0">Body</h4>
                          </li>
                          <li class="p-2">
                            <p class="mb-0 fs-12 text-grey pb-1">font family</p>
                            <div class="dropdown">
                              <button
                                type="button "
                                class="btn p-2 border-0 dropdown-toggle text-white fs-12 d-flex justify-content-between w-100 align-items-center bagDark dropdownBtn"
                                data-bs-toggle="dropdown"
                                @click="toggleDropdown"
                              >
                                {{ selectedFontFamily }}
                              </button>
                              <ul
                                style="{ display: isDropdownOpen ? 'block' : 'none' }"
                                class="dropdown-menu fontmenu"
                              >
                                <li v-for="(font, index) in fontList" :key="index">
                                  <a
                                    class="dropdown-item"
                                    @click="selectFont(font)"
                                    fontfamily="ABeeZee"
                                    :style="{ fontFamily: 'A Bee Zee' }"
                                    >{{ font }}</a
                                  >
                                </li>
                              </ul>
                            </div>
                          </li>
                          <li class="p-2">
                            <div
                              class="d-flex align-items-center justify-content-between"
                            >
                              <p class="fs-12 mb-0">Font Size</p>
                              <input
                                class="form-control bagDark formInput border-0 fs-12 text-white"
                                type="text"
                                name="number"
                                v-model="bodyFontSize"
                                @input="updateStyling"
                                value="14px"
                              />
                            </div>
                          </li>
                          <li class="p-2">
                            <div
                              class="d-flex align-items-center justify-content-between"
                            >
                              <p class="fs-12 mb-0 text-grey">Line Height</p>
                              <input
                                v-model="bodyLineHeight"
                                @input="updateStyling"
                                class="form-control bagDark formInput border-0 fs-12 text-white"
                                type="text"
                                name="text"
                                value="1"
                              />
                            </div>
                          </li>
                          <li class="p-2">
                            <div
                              class="d-flex align-items-center justify-content-between"
                            >
                              <p class="fs-12 mb-0 text-grey">Font Colour</p>
                              <input
                                type="color"
                                v-model="bodyFontColor"
                                @input="updateStyling"
                                class="form-control form-control-color p-0 formInput bgsecondary border-0 fs-12"
                                value="#555555"
                                title="Choose your color"
                              />
                            </div>
                          </li>
                          <li class="p-2">
                            <p class="fs-12 text-grey">Padding</p>
                            <div>
                              <div class="wrapper d-flex flex-wrap">
                                <input
                                  type="text"
                                  v-model="bodyPadding.top"
                                  @input="updateStyling"
                                  placeholder="Top"
                                  value=""
                                  class="top text-center m-auto"
                                />
                                <input
                                  type="text"
                                  v-model="bodyPadding.left"
                                  @input="updateStyling"
                                  placeholder="Left"
                                  value=""
                                  class="left text-center"
                                />
                                <div class="item center-center"></div>
                                <input
                                  type="text"
                                  v-model="bodyPadding.right"
                                  @input="updateStyling"
                                  placeholder="Right"
                                  value=""
                                  class="right text-center"
                                />
                                <input
                                  type="text"
                                  v-model="bodyPadding.bottom"
                                  @input="updateStyling"
                                  placeholder="Bottom"
                                  value=""
                                  class="bottom text-center m-auto"
                                />
                              </div>
                            </div>
                          </li>
                          <li class="p-2">
                            <p class="fs-12 mb-0 text-grey">Background Image</p>
                            <div class="backgroundImage"></div>
                            <div class='mt-3'>
                              <input class='form-control bagDark formInput w-100 border-0 fs-12 text-white' type="text" name="text" value="">
                            </div>
                          </li>
                          <li class="p-2">
                            <p class="fs-12 mb-0 text-grey pb-2">Background Position</p>
                            <select
                             v-model="backgroundPosition"
                                  @change="updateStyling"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Top</option>
                              <option value="2" class="fs-12">Bottom</option>
                              <option value="3" class="fs-12">Left</option>
                              <option value="3" class="fs-12">Right</option>
                            </select>
                          </li>
                          <li class="p-2">
                            <p class="fs-12 mb-0 text-grey pb-2">Background Repeat</p>
                            <select
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected disabled>-</option>
                              <option value="1" class="fs-12">Repeat</option>
                              <option value="2" class="fs-12">Repeat-x</option>
                              <option value="3" class="fs-12">Repeat-y</option>
                              <option value="3" class="fs-12">No-repeat</option>
                            </select>
                          </li>
                          <li class="p-2">
                            <p class="fs-12 mb-0 text-grey pb-2">Background Size</p>
                            <select
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Auto</option>
                              <option value="2" class="fs-12">Cover</option>
                              <option value="3" class="fs-12">Contain</option>
                              <option value="3" class="fs-12">Custom</option>
                            </select>
                          </li>
                          <li class="p-2">
                            <p class="fs-12 mb-0 text-grey pb-2">Background Size</p>
                            <select
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12"></option>
                              <option value="1" class="fs-12">Solid color</option>
                              <option onselect="myFunction()" value="2" class="fs-12">Radial gradient</option>
                              <option value="3" class="fs-12">Horizontal gradient</option>
                              <option value="3" class="fs-12">Vertical gradient</option>
                              <option value="3" class="fs-12">Angle gradient</option>
                            </select>
                            <div class='d-flex'>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bgWhite border-0 fs-12 mt-2 me-1"
                              id="exampleColorInput"
                              value="#ffffff"
                              title="Choose your color"
                            />
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bgWhite border-0 fs-12 mt-2 ms-1"
                              id="exampleColorInput"
                              value="#ffffff"
                              title="Choose your color"
                            /></div>
                          </li>
                        </ul>
                      </div>
                    </div>
                    <div
                      class="tab-pane fade text-white p-2"
                      id="v-pills-profile2"
                      role="tabpanel"
                      aria-labelledby="v-pills-profile-tab2"
                    >
                      <ul class="list-unstyled mb-0">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-secondary activaNavigate mb-0">Sections</h4>
                        </li>
                        <li class="p-2">
                          <p class="fs-12 text-grey">Margin</p>
                          <div>
                            <div class="wrapper d-flex flex-wrap">
                              <input
                                type="text"
                                placeholder="Top"
                                value=""
                                class="top text-center m-auto"
                              /><input
                                type="text"
                                placeholder="Left"
                                value=""
                                class="left text-center"
                              />
                              <div class="item center-center"></div>
                              <input
                                type="text"
                                placeholder="Right"
                                value=""
                                class="right text-center"
                              /><input
                                type="text"
                                placeholder="Bottom"
                                value=""
                                class="bottom text-center m-auto"
                              />
                            </div>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0 text-grey">Separator color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#af9f8c"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <p class="fs-12 mb-0 text-grey pb-2">Default Background</p>
                          <select
                            class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                            aria-label="Default select example"
                          >
                            <option selected>-</option>
                            <option value="1" class="fs-12">Solid color</option>
                            <option value="2" class="fs-12">Radial gradient</option>
                            <option value="3" class="fs-12">Horizontal gradient</option>
                            <option value="3" class="fs-12">Vertical gradient</option>
                            <option value="3" class="fs-12">Angle gradient</option>
                          </select>
                          <input
                            type="color"
                            class="form-control form-control-color p-0 formInput bg-white border-0 fs-12 mt-2"
                            id="exampleColorInput"
                            value="#ffffff"
                            title="Choose your color"
                          />
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane fade text-white p-2"
                      id="v-pills-messages2"
                      role="tabpanel"
                      aria-labelledby="v-pills-messages-tab2"
                    >
                      <ul class="list-unstyled mb-0 pb-5">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-secondary activaNavigate mb-0">H1</h4>
                        </li>
                        <li class="p-2">
                          <p class="mb-0 fs-12 text-grey pb-1">font family</p>
                          <div class="dropdown">
                            <button
                              type="button "
                              class="btn p-2 border-0 dropdown-toggle text-white fs-12 d-flex justify-content-between w-100 align-items-center bagDark dropdownBtn"
                              data-bs-toggle="dropdown"
                              @click="toggleDropdown"
                            >
                              {{ selectedFontFamily }}
                            </button>
                            <ul
                              style="{ display: isDropdownOpen ? 'block' : 'none' }"
                              class="dropdown-menu fontmenu"
                            >
                              <li v-for="(font, index) in fontList" :key="index">
                                <a
                                  class="dropdown-item"
                                  @click="selectFont(font)"
                                  fontfamily="ABeeZee"
                                  :style="{ fontFamily: 'A Bee Zee' }"
                                  >{{ font }}</a
                                >
                              </li>
                            </ul>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Size</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Weight</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Bold</option>
                              <option value="2" class="fs-12">Bolder</option>
                              <option value="3" class="fs-12">Lighter</option>
                              <option value="3" class="fs-12">100</option>
                              <option value="3" class="fs-12">200</option>
                              <option value="3" class="fs-12">300</option>
                              <option value="3" class="fs-12">400</option>
                              <option value="3" class="fs-12">500</option>
                              <option value="3" class="fs-12">600</option>
                              <option value="3" class="fs-12">700</option>
                              <option value="3" class="fs-12">800</option>
                              <option value="3" class="fs-12">900</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Line Height</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Letter Spacing</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Style</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Normal</option>
                              <option value="2" class="fs-12">Italic</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Transform</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">None</option>
                              <option value="2" class="fs-12">Underline</option>
                              <option value="2" class="fs-12">Overline</option>
                              <option value="2" class="fs-12">Line-through</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Decoration</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Capitalize</option>
                              <option value="2" class="fs-12">Uppercase</option>
                              <option value="2" class="fs-12">Lowercase</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bg-black border-0 fs-12"
                              id="exampleColorInput"
                              value="#222222"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <p class="fs-12 pb-1 mb-0">Text Shadow</p>
                          <div
                            class="d-flex align-items-center justify-content-between textShadowInput"
                          >
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="color"
                              class="form-control p-1 formColor form-control-color p-0 bgsecondary border-0 fs-12 text-white"
                              id="exampleColorInput"
                              value="#eeeeee"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                      </ul>
                    </div>

                    <div
                      class="tab-pane fade text-white p-2"
                      id="v-pills-messagesh2"
                      role="tabpanel"
                      aria-labelledby="v-pills-messagesh2-tab2"
                    >
                      <ul class="list-unstyled mb-0 pb-5">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-secondary activaNavigate mb-0">H2</h4>
                        </li>
                        <li class="p-2">
                          <p class="mb-0 fs-12 text-grey pb-1">font family</p>
                          <div class="dropdown">
                            <button
                              type="button "
                              class="btn p-2 border-0 dropdown-toggle text-white fs-12 d-flex justify-content-between w-100 align-items-center bagDark dropdownBtn"
                              data-bs-toggle="dropdown"
                              @click="toggleDropdown"
                            >
                              {{ selectedFontFamily }}
                            </button>
                            <ul
                              style="{ display: isDropdownOpen ? 'block' : 'none' }"
                              class="dropdown-menu fontmenu"
                            >
                              <li v-for="(font, index) in fontList" :key="index">
                                <a
                                  class="dropdown-item"
                                  @click="selectFont(font)"
                                  fontfamily="ABeeZee"
                                  :style="{ fontFamily: 'A Bee Zee' }"
                                  >{{ font }}</a
                                >
                              </li>
                            </ul>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Size</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Weight</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Bold</option>
                              <option value="2" class="fs-12">Bolder</option>
                              <option value="3" class="fs-12">Lighter</option>
                              <option value="3" class="fs-12">100</option>
                              <option value="3" class="fs-12">200</option>
                              <option value="3" class="fs-12">300</option>
                              <option value="3" class="fs-12">400</option>
                              <option value="3" class="fs-12">500</option>
                              <option value="3" class="fs-12">600</option>
                              <option value="3" class="fs-12">700</option>
                              <option value="3" class="fs-12">800</option>
                              <option value="3" class="fs-12">900</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Line Height</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Letter Spacing</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Style</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Normal</option>
                              <option value="2" class="fs-12">Italic</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Transform</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">None</option>
                              <option value="2" class="fs-12">Underline</option>
                              <option value="2" class="fs-12">Overline</option>
                              <option value="2" class="fs-12">Line-through</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Decoration</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Capitalize</option>
                              <option value="2" class="fs-12">Uppercase</option>
                              <option value="2" class="fs-12">Lowercase</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bg-black border-0 fs-12"
                              id="exampleColorInput"
                              value="#222222"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <p class="fs-12 pb-1 mb-0">Text Shadow</p>
                          <div
                            class="d-flex align-items-center justify-content-between textShadowInput"
                          >
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="color"
                              class="form-control p-1 formColor form-control-color p-0 bgsecondary border-0 fs-12 text-white"
                              id="exampleColorInput"
                              value="#eeeeee"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane fade text-white p-2"
                      id="v-pills-messagesh3"
                      role="tabpanel"
                      aria-labelledby="v-pills-messagesh1-tab2"
                    >
                      <ul class="list-unstyled mb-0 pb-5">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-secondary activaNavigate mb-0">H3</h4>
                        </li>
                        <li class="p-2">
                          <p class="mb-0 fs-12 text-grey pb-1">font family</p>
                          <div class="dropdown">
                            <button
                              type="button "
                              class="btn p-2 border-0 dropdown-toggle text-white fs-12 d-flex justify-content-between w-100 align-items-center bagDark dropdownBtn"
                              data-bs-toggle="dropdown"
                              @click="toggleDropdown"
                            >
                              {{ selectedFontFamily }}
                            </button>
                            <ul
                              style="{ display: isDropdownOpen ? 'block' : 'none' }"
                              class="dropdown-menu fontmenu"
                            >
                              <li v-for="(font, index) in fontList" :key="index">
                                <a
                                  class="dropdown-item"
                                  @click="selectFont(font)"
                                  fontfamily="ABeeZee"
                                  :style="{ fontFamily: 'A Bee Zee' }"
                                  >{{ font }}</a
                                >
                              </li>
                            </ul>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Size</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Weight</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Bold</option>
                              <option value="2" class="fs-12">Bolder</option>
                              <option value="3" class="fs-12">Lighter</option>
                              <option value="3" class="fs-12">100</option>
                              <option value="3" class="fs-12">200</option>
                              <option value="3" class="fs-12">300</option>
                              <option value="3" class="fs-12">400</option>
                              <option value="3" class="fs-12">500</option>
                              <option value="3" class="fs-12">600</option>
                              <option value="3" class="fs-12">700</option>
                              <option value="3" class="fs-12">800</option>
                              <option value="3" class="fs-12">900</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Line Height</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Letter Spacing</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Style</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Normal</option>
                              <option value="2" class="fs-12">Italic</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Transform</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">None</option>
                              <option value="2" class="fs-12">Underline</option>
                              <option value="2" class="fs-12">Overline</option>
                              <option value="2" class="fs-12">Line-through</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Decoration</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Capitalize</option>
                              <option value="2" class="fs-12">Uppercase</option>
                              <option value="2" class="fs-12">Lowercase</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bg-black border-0 fs-12"
                              id="exampleColorInput"
                              value="#222222"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <p class="fs-12 pb-1 mb-0">Text Shadow</p>
                          <div
                            class="d-flex align-items-center justify-content-between textShadowInput"
                          >
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="color"
                              class="form-control p-1 formColor form-control-color p-0 bgsecondary border-0 fs-12 text-white"
                              id="exampleColorInput"
                              value="#eeeeee"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane fade text-white p-2"
                      id="v-pills-messagesh4"
                      role="tabpanel"
                      aria-labelledby="v-pills-messagesh4-tab2"
                    >
                      <ul class="list-unstyled mb-0 pb-5">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-secondary activaNavigate mb-0">H4</h4>
                        </li>
                        <li class="p-2">
                          <p class="mb-0 fs-12 text-grey pb-1">font family</p>
                          <div class="dropdown">
                            <button
                              type="button "
                              class="btn p-2 border-0 dropdown-toggle text-white fs-12 d-flex justify-content-between w-100 align-items-center bagDark dropdownBtn"
                              data-bs-toggle="dropdown"
                              @click="toggleDropdown"
                            >
                              {{ selectedFontFamily }}
                            </button>
                            <ul
                              style="{ display: isDropdownOpen ? 'block' : 'none' }"
                              class="dropdown-menu fontmenu"
                            >
                              <li v-for="(font, index) in fontList" :key="index">
                                <a
                                  class="dropdown-item"
                                  @click="selectFont(font)"
                                  fontfamily="ABeeZee"
                                  :style="{ fontFamily: 'A Bee Zee' }"
                                  >{{ font }}</a
                                >
                              </li>
                            </ul>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Size</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Weight</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Bold</option>
                              <option value="2" class="fs-12">Bolder</option>
                              <option value="3" class="fs-12">Lighter</option>
                              <option value="3" class="fs-12">100</option>
                              <option value="3" class="fs-12">200</option>
                              <option value="3" class="fs-12">300</option>
                              <option value="3" class="fs-12">400</option>
                              <option value="3" class="fs-12">500</option>
                              <option value="3" class="fs-12">600</option>
                              <option value="3" class="fs-12">700</option>
                              <option value="3" class="fs-12">800</option>
                              <option value="3" class="fs-12">900</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Line Height</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Letter Spacing</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Style</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Normal</option>
                              <option value="2" class="fs-12">Italic</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Transform</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">None</option>
                              <option value="2" class="fs-12">Underline</option>
                              <option value="2" class="fs-12">Overline</option>
                              <option value="2" class="fs-12">Line-through</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Decoration</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Capitalize</option>
                              <option value="2" class="fs-12">Uppercase</option>
                              <option value="2" class="fs-12">Lowercase</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bg-black border-0 fs-12"
                              id="exampleColorInput"
                              value="#222222"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <p class="fs-12 pb-1 mb-0">Text Shadow</p>
                          <div
                            class="d-flex align-items-center justify-content-between textShadowInput"
                          >
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="text"
                              placeholder="-"
                              value=""
                              class="bagDark border-0 p-2 text-white fs-12"
                            />
                            <input
                              type="color"
                              class="form-control p-1 formColor form-control-color p-0 bgsecondary border-0 fs-12 text-white"
                              id="exampleColorInput"
                              value="#eeeeee"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane fade text-white p-2"
                      id="v-pills-link"
                      role="tabpanel"
                      aria-labelledby="v-pills-link-tab2"
                    >
                      <ul class="list-unstyled">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-secondary activaNavigate mb-0">Links</h4>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0 text-grey">Color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bgsecondary border-0 fs-12"
                              id="exampleColorInput"
                              value="#555555"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0 text-grey">Text Decoration</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12 text-grey">
                                Capitalize
                              </option>
                              <option value="2" class="fs-12 text-grey">Uppercase</option>
                              <option value="2" class="fs-12 text-grey">Lowercase</option>
                              <option value="2" class="fs-12 text-grey">
                                Line-through
                              </option>
                              <option value="2" class="fs-12 text-grey">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0 text-grey">Hover Color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bgsecondary border-0 fs-12"
                              id="exampleColorInput"
                              value="#555555"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 text-grey mb-0">Hover Text Decoration</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12 text-grey">
                                Capitalize
                              </option>
                              <option value="2" class="fs-12 text-grey">Uppercase</option>
                              <option value="2" class="fs-12 text-grey">Lowercase</option>
                              <option value="2" class="fs-12 text-grey">
                                Line-through
                              </option>
                              <option value="2" class="fs-12 text-grey">Inherit</option>
                            </select>
                          </div>
                        </li>
                      </ul>
                    </div>

                    <div
                      class="tab-pane fade text-white pt-2"
                      id="v-pills-Buttons"
                      role="tabpanel"
                      aria-labelledby="v-pills-Buttons-tab2"
                    >
                      <ul class="list-unstyled mb-0 pb-5">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-secondary activaNavigate mb-0">Buttons</h4>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Size</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Weight</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">Bold</option>
                              <option value="2" class="fs-12">Bolder</option>
                              <option value="3" class="fs-12">Lighter</option>
                              <option value="3" class="fs-12">100</option>
                              <option value="3" class="fs-12">200</option>
                              <option value="3" class="fs-12">300</option>
                              <option value="3" class="fs-12">400</option>
                              <option value="3" class="fs-12">500</option>
                              <option value="3" class="fs-12">600</option>
                              <option value="3" class="fs-12">700</option>
                              <option value="3" class="fs-12">800</option>
                              <option value="3" class="fs-12">900</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Line Height</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Letter Spacing</p>
                            <input
                              class="form-control bagDark formInput border-0 fs-12 text-white"
                              type="text"
                              name="text"
                              value="14px"
                            />
                          </div>
                        </li>

                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text Transform</p>
                            <select
                              style="width: 100px !important"
                              class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                              aria-label="Default select example"
                            >
                              <option selected>-</option>
                              <option value="1" class="fs-12">None</option>
                              <option value="2" class="fs-12">Underline</option>
                              <option value="2" class="fs-12">Overline</option>
                              <option value="2" class="fs-12">Line-through</option>
                              <option value="2" class="fs-12">Inherit</option>
                            </select>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput bg-black border-0 fs-12"
                              id="exampleColorInput"
                              value="#222222"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <p class="fs-12 text-grey">Border Radius</p>
                          <div>
                            <div class="wrapper d-flex flex-wrap">
                              <input
                                type="text"
                                value=""
                                placeholder="Top"
                                class="top text-center m-auto"
                              /><input
                                type="text"
                                placeholder="left"
                                value=""
                                class="left text-center"
                              />
                              <div class="item centerBorder rounded"></div>
                              <input
                                type="text"
                                placeholder="right"
                                value=""
                                class="right text-center"
                              /><input
                                type="text"
                                value=""
                                placeholder="Bottom"
                                class="bottom text-center m-auto"
                              />
                            </div>
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <p class="fs-12 text-grey">Border Width</p>
                          <div>
                            <div class="wrapper d-flex flex-wrap">
                              <input
                                type="text"
                                value=""
                                placeholder="Top"
                                class="top text-center m-auto"
                              /><input
                                type="text"
                                placeholder="left"
                                value=""
                                class="left text-center"
                              />
                              <div class="item centerBorder"></div>
                              <input
                                type="text"
                                placeholder="right"
                                value=""
                                class="right text-center"
                              /><input
                                type="text"
                                value=""
                                placeholder="Bottom"
                                class="bottom text-center m-auto"
                              />
                            </div>
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane fade text-white"
                      id="v-pills-Buttonsprimary"
                      role="tabpanel"
                      aria-labelledby="v-pills-Buttonsprimary-tab2"
                    >
                      <ul class="p-2 mb-1 list-unstyled">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-grey ry activaNavigate mb-0">
                            Buttons Primary
                          </h4>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formColor formInput border-0 fs-12"
                              id="exampleColorInput"
                              value="#ffffff"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font :hover</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput formColor border-0 fs-12"
                              id="exampleColorInput"
                              value="#ffffff"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">
                              Font <br />
                              Outline
                            </p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#af9f8c"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Outline:Hover</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#998b7a"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Border</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#998b7a"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Border:Hover</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#998b7a"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2">
                          <p class="fs-12 mb-0 text-grey pb-2">Background</p>
                          <select
                            class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                            aria-label="Default select example"
                          >
                            <option selected>-</option>
                            <option value="1" class="fs-12"></option>
                            <option value="1" class="fs-12">Solid color</option>
                            <option value="2" class="fs-12">Radial gradient</option>
                            <option value="3" class="fs-12">Horizontal gradient</option>
                            <option value="3" class="fs-12">Vertical gradient</option>
                            <option value="3" class="fs-12">Angle gradient</option>
                          </select>
                          <input
                            type="color"
                            class="form-control form-control-color p-0 formInput lightolor border-0 fs-12 mt-2"
                            id="exampleColorInput"
                            value="#998b7a"
                            title="Choose your color"
                          />
                        </li>
                        <li class="p-2">
                          <p class="fs-12 mb-0 text-grey pb-2">Background:Hover</p>
                          <select
                            class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                            aria-label="Default select example"
                          >
                            <option selected>-</option>
                            <option value="1" class="fs-12"></option>
                            <option value="1" class="fs-12">Solid color</option>
                            <option value="2" class="fs-12">Radial gradient</option>
                            <option value="3" class="fs-12">Horizontal gradient</option>
                            <option value="3" class="fs-12">Vertical gradient</option>
                            <option value="3" class="fs-12">Angle gradient</option>
                          </select>
                          <input
                            type="color"
                            class="form-control form-control-color p-0 formInput lightolor border-0 fs-12 mt-2"
                            id="exampleColorInput"
                            value="#998b7a"
                            title="Choose your color"
                          />
                        </li>
                      </ul>
                    </div>
                    <div
                      class="tab-pane fade text-white"
                      id="v-pills-Buttonsecondary"
                      role="tabpanel"
                      aria-labelledby="v-pills-Buttonsecondary-tab2"
                    >
                      <ul class="p-2 mb-1 list-unstyled">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-grey ry activaNavigate mb-0">
                            Buttons Primary
                          </h4>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formColor formInput border-0 fs-12"
                              id="exampleColorInput"
                              value="#ffffff"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font :hover</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput formColor border-0 fs-12"
                              id="exampleColorInput"
                              value="#ffffff"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Font Outline</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#91989f"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Outline:Hover</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#91989f"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Border</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#91989f"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Border:Hover</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#91989f"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2">
                          <p class="fs-12 mb-0 text-grey pb-2">Background</p>
                          <select
                            class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                            aria-label="Default select example"
                          >
                            <option selected>-</option>
                            <option value="1" class="fs-12"></option>
                            <option value="1" class="fs-12">Solid color</option>
                            <option value="2" class="fs-12">Radial gradient</option>
                            <option value="3" class="fs-12">Horizontal gradient</option>
                            <option value="3" class="fs-12">Vertical gradient</option>
                            <option value="3" class="fs-12">Angle gradient</option>
                          </select>
                          <input
                            type="color"
                            class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12 mt-2"
                            id="exampleColorInput"
                            value="#91989f"
                            title="Choose your color"
                          />
                        </li>
                        <li class="p-2">
                          <p class="fs-12 mb-0 text-grey pb-2">Background:Hover</p>
                          <select
                            class="form-select bagDark border-0 text-white formInput w-100 fs-12"
                            aria-label="Default select example"
                          >
                            <option selected>-</option>
                            <option value="1" class="fs-12"></option>
                            <option value="1" class="fs-12">Solid color</option>
                            <option value="2" class="fs-12">Radial gradient</option>
                            <option value="3" class="fs-12">Horizontal gradient</option>
                            <option value="3" class="fs-12">Vertical gradient</option>
                            <option value="3" class="fs-12">Angle gradient</option>
                          </select>
                          <input
                            type="color"
                            class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12 mt-2"
                            id="exampleColorInput"
                            value="#91989f"
                            title="Choose your color"
                          />
                        </li>
                      </ul>
                    </div>

                    <div
                      class="tab-pane fade text-white"
                      id="v-pills-Other"
                      role="tabpanel"
                      aria-labelledby="v-pills-Other-tab2"
                    >
                      <ul class="p-2 mb-1 list-unstyled">
                        <li
                          data-group="navigations"
                          class="active bold p-2 d-flex justify-content-between mt-1"
                        >
                          <h4 class="text-grey ry activaNavigate mb-0">Others</h4>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Border color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#91989f"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Border-x2 color</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#91989f"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text primary</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#af9f8c"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                        <li class="p-2 mt-1">
                          <div class="d-flex align-items-center justify-content-between">
                            <p class="fs-12 mb-0">Text secondary</p>
                            <input
                              type="color"
                              class="form-control form-control-color p-0 formInput lightbluecolor border-0 fs-12"
                              id="exampleColorInput"
                              value="#91989f"
                              title="Choose your color"
                            />
                          </div>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>

              <div
                class="tab-pane p-2 fade text-white"
                id="v-pills-messages"
                role="tabpanel"
                aria-labelledby="v-pills-messages-tab"
              ></div>
            </div>
          </div>
        </div>

        <div class="d-none element_list col-lg-2">
          <button
            class="btn btn-primary w-50 d-block"
            data-type="HeaderComponent"
            draggable="true"
            @dragstart="handleDragStart"
          >
            Header
          </button>
          <button
            class="btn btn-primary w-50 mt-3 d-block"
            data-type="CardsComponent"
            draggable="true"
            @dragstart="handleDragStart"
          >
            Cards
          </button>
          <button
            class="btn btn-primary w-50 mt-3 d-block"
            data-type="FooterComponent"
            draggable="true"
            @dragstart="handleDragStart"
          >
            Footer
          </button>
          <button
            class="btn btn-primary w-50 mt-3 d-block"
            @click="toggleMode('preview')"
          >
            Preview
          </button>
          <button class="btn btn-primary w-50 mt-3 d-block" @click="toggleMode('edit')">
            Edit
          </button>
        </div>

        <div
          ref="dropzone"
          class="border bodySection borderDark w-100"
          @dragover.prevent="handleDragOver"
          @drop="handleDrop"
        >
          <!-- Your dropped components will go here -->
          <div
            v-for="(component, index) in components"
            :key="index"
            @mouseover="setHovered(index, true)"
            class="position-relative"
            @mouseleave="setHovered(index, false)"
          >
            <component :is="component.type" v-bind="component.props" />
            <div
              v-if="mode === 'edit' && hoveredComponent === index"
              class="position-absolute d-flex edit-code-button justify-content-center align-items-center w-100 top-0 h-100"
            >
              <button @click="cloneComponent(index)" class="btn bg-dark">
                <img src="./assets/images/copy.svg" alt="" />
              </button>
              <button @click="deleteComponent(index)" class="btn bg-dark mx-1">
                <img src="./assets/images/trash.svg" alt="" />
              </button>
              <button @click="editComponentCode(index)" class="btn bg-dark">
                <img src="./assets/images/code.svg" alt="" />
              </button>
              <button @click="placeTop(index)" class="btn bg-dark mx-1">
                <img src="./assets/images/arrow-up.svg" alt="" />
              </button>
              <button @click="placeBottom(index)" class="btn bg-dark">
                <img src="./assets/images/arrow-down.svg" alt="" />
              </button>
            </div>
          </div>
        </div>
        <!-- Modal -->
        <div
          v-if="showCodeMirrorPopup"
          :class="{ 'codemirror-popup': true, animate__fadeInDown: showCodeMirrorPopup }"
        >
          <div class="codemirror-popup-inner">
            <div class="d-flex justify-content-between position-relative">
              <h5 class="supra mb-3">Section code editor</h5>
              <button type="button" class="btn-close" @click="closeModel(index)"></button>
            </div>
            <Codemirror
              v-model:value="selectedComponentCode"
              :options="cmOptions"
              placeholder="test placeholder"
              :height="500"
              @change="change"
            />
            <div class="d-flex">
              <button
                @click="saveCode"
                class="btn btn-dark mt-2 w-50 py-2 rounded-0 text-white"
              >
                Cancel
              </button>
              <button
                @click="saveCode"
                class="btn btn-info mt-2 py-2 w-50 rounded-0 text-white"
              >
                Apply
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import CardOne from "./webbuildcom/CardOne.vue";
import CardTwo from "./webbuildcom/CardTwo.vue";
import CardThree from "./webbuildcom/CardThree.vue";
import CardFour from "./webbuildcom/CardFour.vue";
import CardFive from "./webbuildcom/CardFive.vue";
import CardSix from "./webbuildcom/CardSix.vue";
import ListOne from "./webbuildcom/ListOne.vue";
import ListTwo from "./webbuildcom/ListTwo.vue";
import ListThree from "./webbuildcom/ListThree.vue";
import ListFour from "./webbuildcom/ListFour.vue";
import ListFive from "./webbuildcom/ListFive.vue";
import ListSix from "./webbuildcom/ListSix.vue";
import ListSeven from "./webbuildcom/ListSeven.vue";
// import ListEight from "./webbuildcom/ListEight.vue";
// import ListNine from "./webbuildcom/ListNine.vue";
// import ListTen from "./webbuildcom/ListTen.vue";
// import ListEleven from "./webbuildcom/ListEleven.vue";
// import ListTwelve from "./webbuildcom/ListTwelve.vue";
// import ListThirteen from "./webbuildcom/ListThirteen.vue";
// import ListFourteen from "./webbuildcom/ListFourteen.vue";
// import ListFifteen from "./webbuildcom/ListFifteen.vue";
// import ListSixteen from "./webbuildcom/ListSixteen.vue";
import Codemirror from "codemirror-editor-vue3";
import "codemirror/addon/display/placeholder.js";
import "codemirror/mode/javascript/javascript.js";
import "codemirror/addon/display/placeholder.js";
import "codemirror/theme/dracula.css";
import "./assets/css/index.css";
import "./assets/css/style.css";
export default {
  data() {
    return {
      isDropdownOpen: false,
      showCodeMirrorPopup: false,
      selectedFontFamily: "open sans",
      bodyFontSize: "14",
      bodyLineHeight: "1",
      bodyFontColor: "#555555",
      backgroundRepeat: "repeat",
      backgroundPosition: 'center',
      bodyPadding: {
        top: 0,
        right: 0,
        bottom: 0,
        left: 0,
      },
      fontList: [
        "ABeeZee",
        "Abel",
        "AbrilFatface",
        "Acme",
        "Alegreya",
        "Amaranth",
        "AmaticSC",
        "Anton",
        "ArchivoBlack",
        "ArchivoNarrow",
        "Arimo",
        "Arvo",
        "Asap",
        "Bahiana",
        "BerkshireSwash",
        "Bitter",
        "BreeSerif",
        "Bungee",
        "Cabin",
        "CabinSketch",
        "Cairo",
        "Catamaran",
        "Chewy",
        "Cinzel",
        "Comfortaa",
        "CormorantGaramond",
        "Creepster",
        "CreteRound",
        "CrimsonText",
        "Cuprum",
        "CutiveMono",
        "DancingScript",
        "DidactGothic",
        "Dosis",
        "EBGaramond",
        "Exo",
        "Exo2",
        "FiraSans",
        "FjallaOne",
        "FontdinerSwanky",
        "FrancoisOne",
        "FrederickatheGreat",
        "FugazOne",
        "Geo",
        "Graduate",
        "Handlee",
        "Hind",
        "AbrilFatface",
        "Acme",
        "Alegreya",
        "Amaranth",
        "AmaticSC",
        "Anton",
        "ArchivoBlack",
        "ArchivoNarrow",
        "Arimo",
        "Arvo",
        "HindSiliguri",
        "Inconsolata",
        "JosefinSans",
        "JosefinSlab",
        "JuliusSansOne",
        "Kanit",
        "Karla",
        "KaushanScript",
        "KumarOneLato",
        "LibreBaskerville",
        "LibreFranklin",
        "LifeSavers",
        "Lobster",
        "Lora",
        "MavenPro",
        "Merriweather",
        "MerriweatherSan",
        "Modak",
        "Monoton",
        "Montserrat",
        "Muli",
        "NanumGothic",
        "NotoSans",
        "NotoSerif",
        "Nunito",
        "NunitoSans",
        "OldStandard",
        "OpenSans",
        "OpenSansCondensed",
        "Oswald",
        "Oxygen",
        "Pacifico",
        "PathwayGothicOne",
        "PatuaOne",
        "PermanentMarker",
        "Play",
        "PlayfairDisplay",
        "PoiretOne",
        "Poppins",
        "Prata",
        "Quattrocento",
        "Questrial",
        "Quicksand",
        "RacingSansOne",
        "Rajdhani",
        "Asap",
        "Bahiana",
        "BerkshireSwash",
        "Bitter",
        "BreeSerif",
        "Bungee",
        "Cabin",
        "CabinSketch",
        "Cairo",
        "Catamaran",
        "Chewy",
        "Raleway",
        "Righteous",
        "Roboto",
        "RobotoCondensed",
        "RobotoMono",
        "Rokkitt",
        "Rubik",
        "Rufina",
        "Rye",
        "Sancreek",
        "ShadowsInto",
        "Shrikhand",
        "Signika",
        "Slabo27px",
        "SourceCodePro",
        "SourceSansPro",
        "SourceSerifPro",
        "Ubuntu",
        "UbuntuCondensed",
        "UnifrakturCook",
        "VT323",
        "VarelaRound",
        "Vidaloka",
        "Vollkorn",
        "WorkSans",
        "YanoneKaffeesatz",
        "ZillaSlab",
      ],
      selectedComponentCode: "", // Add this line
      draggedComponent: null,
      components: [],
      hoveredComponent: null,
      mode: "edit",
      cmOptions: {
        mode: "text/javascript", // Language mode
        theme: "dracula", // Theme
      },
    };
  },

  components: { Codemirror },

  methods: {
    updateStyling() {
      document.documentElement.style.setProperty(
        "--bodyfontHeight",
        `${this.bodyLineHeight}px`
      );
      document.documentElement.style.setProperty(
        "--bodyfontColor",
        `${this.bodyFontColor}`
      );
      document.documentElement.style.setProperty(
        "--bodyfontSize",
        `${this.bodyFontSize}px`
      );
       document.documentElement.style.setProperty(
        "--bodybackgroundPosition",
        `${this.backgroundPosition}`
      );
      // Body Padding
      const { top, right, bottom, left } = this.bodyPadding;
      document.documentElement.style.setProperty("--body-padding-top", `${top}px`);
      document.documentElement.style.setProperty("--body-padding-right", `${right}px`);
      document.documentElement.style.setProperty("--body-padding-bottom", `${bottom}px`);
      document.documentElement.style.setProperty("--body-padding-left", `${left}px`);
      // Body Padding
    },
    handleDragStart(event) {
      this.draggedComponent = event.target.dataset.type;
    },
    toggleDropdown() {
      this.isDropdownOpen = !this.isDropdownOpen;
    },
    selectFont(font) {
      this.selectedFontFamily = font;

      this.isDropdownOpen = false;
    },
    handleDragOver(event) {
      event.preventDefault();
    },
    handleDrop(event) {
      event.preventDefault();

      if (this.draggedComponent) {
        const mouseY = event.clientY;

        let newComponent;
        // Inside the handleDrop method
        switch (this.draggedComponent) {
          case "CardOne":
            newComponent = { type: CardOne, props: {}, code: "" };
            break;
          case "CardTwo":
            newComponent = { type: CardTwo, props: {}, code: "" };
            break;
          case "CardThree":
            newComponent = { type: CardThree, props: {}, code: "" };
            break;
          case "CardFour":
            newComponent = { type: CardFour, props: {}, code: "" };
            break;
          case "CardFive":
            newComponent = { type: CardFive, props: {}, code: "" };
            break;
          case "CardSix":
            newComponent = { type: CardSix, props: {}, code: "" };
            break;
          case "ListOne":
            newComponent = { type: ListOne, props: {}, code: "" };
            break;
          case "ListTwo":
            newComponent = { type: ListTwo, props: {}, code: "" };
            break;
          case "ListThree":
            newComponent = { type: ListThree, props: {}, code: "" };
            break;
          case "ListFour":
            newComponent = { type: ListFour, props: {}, code: "" };
            break;
          case "ListFive":
            newComponent = { type: ListFive, props: {}, code: "" };
            break;
          case "ListSix":
            newComponent = { type: ListSix, props: {}, code: "" };
            break;
          case "ListSeven":
            newComponent = { type: ListSeven, props: {}, code: "" };
            break;
          case "ListEight":
            newComponent = { type: ListEight, props: {}, code: "" };
            break;
          case "ListTen":
            newComponent = { type: ListTen, props: {}, code: "" };
            break;
          case "ListNine":
            newComponent = { type: ListNine, props: {}, code: "" };
            break;
          case "ListEleven":
            newComponent = { type: ListEleven, props: {}, code: "" };
            break;
          case "ListTwelve":
            newComponent = { type: ListTwelve, props: {}, code: "" };
            break;
          case "ListThirteen":
            newComponent = { type: ListThirteen, props: {}, code: "" };
            break;
          case "ListFourteen":
            newComponent = { type: ListFourteen, props: {}, code: "" };
            break;
          case "ListFifteen":
            newComponent = { type: ListFifteen, props: {}, code: "" };
            break;
          case "ListSixteen":
            newComponent = { type: ListSixteen, props: {}, code: "" };
            break;

          default:
            // Handle other types if needed
            break;
        }

        // Find the index to insert the new component based on mouseY
        const indexToInsert = this.findIndexToInsert(mouseY);

        // Insert the new component at the determined position
        this.components.splice(indexToInsert, 0, newComponent);

        this.draggedComponent = null;
      }
    },
    findIndexToInsert(mouseY) {
      // Find the index to insert the new component based on mouseY
      const dropzoneChildren = this.$refs.dropzone.children;
      for (let i = 0; i < dropzoneChildren.length; i++) {
        const componentRect = dropzoneChildren[i].getBoundingClientRect();
        const componentMidY = componentRect.top + componentRect.height / 2;

        if (mouseY < componentMidY) {
          return i;
        }
      }

      // If mouseY is below all existing components, insert at the end
      return dropzoneChildren.length;
    },
    cloneComponent(index) {
      const clonedComponent = { ...this.components[index] };
      this.components.splice(index + 1, 0, clonedComponent);
    },
    deleteComponent(index) {
      this.components.splice(index, 1);
      this.selectedComponentCode = "";
    },
    setHovered(index, value) {
      this.hoveredComponent = value ? index : null;
      console.log("Hovered Component:", this.hoveredComponent);
    },
    toggleMode(newMode) {
      this.mode = newMode;
    },
    editComponentCode(index) {
      const component = this.components[index];
      const componentCode = this.generateComponentCode(component);
      this.selectedComponentCode = componentCode;
      this.showCodeMirrorPopup = true; // Show the popup
    },
    generateComponentCode(component) {
      if (!component || !component.type) {
        return ""; // Return an empty string if the component or its type is not provided
      }

      const { type } = component;

      // Check if the component has an htmlCode property
      if (type.htmlCode) {
        return type.htmlCode;
      }

      return ""; // Return an empty string if htmlCode is not defined
    },
    // Inside your methods section
    placeTop(index) {
      if (index > 0) {
        const movedComponent = this.components.splice(index, 1)[0];
        this.components.splice(index - 1, 0, movedComponent);
      }
    },
    placeBottom(index) {
      if (index < this.components.length - 1) {
        const movedComponent = this.components.splice(index, 1)[0];
        this.components.splice(index + 1, 0, movedComponent);
      }
    },
    saveCode() {
      console.log("Hovered Component:", this.hoveredComponent);
      this.showCodeMirrorPopup = false;
    },
    closeModel() {
      this.showCodeMirrorPopup = false;
    },
  },
};
</script>
<style scoped>
.codemirror-popup {
  position: fixed;
  top: 50%;
  left: 60%;
  transform: translate(-50%, -50%);
  padding: 20px;
  background-color: #00000073;
  border: 1px solid #ccc;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  z-index: +9999;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.animate__fadeInDown {
  -webkit-animation-name: fadeInDown;
  animation-name: fadeInDown;
}

.btn-close {
  background-color: #444;
  opacity: 0.5 !important;
  top: -30px;
  right: -30px;
  position: absolute;
  cursor: pointer;
  background-image: url('./assets/images/cross.svg');
}

.codemirror-popup-inner {
  width: 50%;
  background-color: #555;
  padding: 30px;
}

.supra {
  color: #888888;
}

@-webkit-keyframes fadeInDown {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, -100%, 0);
    transform: translate3d(0, -100%, 0);
  }

  to {
    opacity: 1;
    -webkit-transform: translateZ(0);
    transform: translateZ(0);
  }
}

.sticky-index {
  z-index: +9999;
}

:root {
  --bodyfontFamily: 'Poppins', sans-serif;
  --bodyfontSize: 16px;
  --bodyfontColor: transparent;
  --bodyfontWeight: inherit;
  --bodyfontHeight: 1;
  --bodyfontPadding: inherit;
  --bodyBackground: light;
  --bodybackgroundPosition: center;
  --bodybackgroundRepeat: repaet;
  --bodybackgroundSize: cover;
  --body-padding-top:0,
  --body-padding-right:0,
  --body-padding-bottom:0,
  --body-padding-left:0,
}

.bodySection {
  font-family: var(--bodyfontFamily);
  font-size: var(--bodyfontSize);
  color: var(--bodyfontColor);
  font-weight: var(--bodyfontWeight);
  line-height: var(--bodyfontHeight);
  padding: var(--body-padding-top) var(--body-padding-right) var(--body-padding-bottom) var(--body-padding-left) ;
  
  background: var(--bodyBackground);
  background-repeat: var(--bodybackgroundRepeat);
  background-position: var(--bodybackgroundPosition);
  background-size: var(--bodyfontSize);
}

:root {
  --sectionMargin: 10px;
  --sectionBackgroundColor: transparent;
  --sectionBackgroundPosition: vertical;
}

section {
  margin: var(--sectionMargin);
  background-color: var(--sectionBackgroundColor);
  background-position: var(--sectionBackgroundPosition);
}

:root {
  --h1fontFamily: 'Poppins', sans-serif;
  --h1fontSize: 16px;
  --h1fontColor: transparent;
  --h1fontWeight: inherit;
  --h1fontHeight: 2;
  --h1fontStyle: normal;
  --h1LetterSpacing: 2px;
  --h1TextDeoration: inherit;
  --h1TextTransform: Inherit;
  --h1textShadow: none;
}

h1 {
  font-family: var(--h1fontFamily);
  font-size: var(--h1fontSize);
  line-height: var(--h1fontHeight);
  font-weight: var(--h1fontWeight);
  font-style: var(--h1fontStyle);
  text-transform: var(--h1TextTransform);
  text-decoration: var(--h1TextDeoration);
  letter-spacing: var(--h1LetterSpacing);
  text-shadow: var(--h1textShadow);
  color: var(--h1fontColor);
}

:root {
  --h2fontFamily: 'Poppins', sans-serif;
  --h2fontSize: 16px;
  --h2fontColor: transparent;
  --h2fontWeight: inherit;
  --h2fontHeight: 2;
  --h2fontStyle: normal;
  --h2LetterSpacing: 2px;
  --h2TextDeoration: inherit;
  --h2TextTransform: Inherit;
  --h2textShadow: none;
}

h2 {
  font-family: var(--h2fontFamily);
  font-size: var(--h2fontSize);
  line-height: var(--h2fontHeight);
  font-weight: var(--h2fontWeight);
  font-style: var(--h2fontStyle);
  text-transform: var(--h2TextTransform);
  text-decoration: var(--h2TextDeoration);
  letter-spacing: var(--h2LetterSpacing);
  text-shadow: var(--h2textShadow);
  color: var(--h2fontColor);
}

:root {
  --h3fontFamily: 'Poppins', sans-serif;
  --h3fontSize: 16px;
  --h3fontColor: transparent;
  --h3fontWeight: inherit;
  --h3fontHeight: 2;
  --h3fontStyle: normal;
  --h3LetterSpacing: 2px;
  --h3TextDeoration: inherit;
  --h3TextTransform: Inherit;
  --h3textShadow: none;
}

h3 {
  font-family: var(--h3fontFamily);
  font-size: var(--h3fontSize);
  line-height: var(--h3fontHeight);
  font-weight: var(--h3fontWeight);
  font-style: var(--h3fontStyle);
  text-transform: var(--h3TextTransform);
  text-decoration: var(--h3TextDeoration);
  letter-spacing: var(--h3LetterSpacing);
  text-shadow: var(--h3textShadow);
  color: var(--h3fontColor);
}

:root {
  --h4fontFamily: 'Poppins', sans-serif;
  --h4fontSize: 16px;
  --h4fontColor: transparent;
  --h4fontWeight: inherit;
  --h4fontHeight: 2;
  --h4fontStyle: normal;
  --h4LetterSpacing: 2px;
  --h4TextDeoration: inherit;
  --h4TextTransform: Inherit;
  --h4textShadow: none;
}

h4 {
  font-family: var(--h4fontFamily);
  font-size: var(--h4fontSize);
  line-height: var(--h4fontHeight);
  font-weight: var(--h4fontWeight);
  font-style: var(--h4fontStyle);
  text-transform: var(--h4TextTransform);
  text-decoration: var(--h4TextDeoration);
  letter-spacing: var(--h4LetterSpacing);
  text-shadow: var(--h4textShadow);
  color: var(--h4fontColor);
}

:root {
  --linkColor: #aaaaaa !important;
  --linkHoverColor: transparent;
  --linkTextDecoration: inherit;
  --linkHoverTextDecoration: normal;
}

a {
  color: var(--linkColor);
  text-decoration: var(--linkTextDecoration);
}

a:hover {
  color: var(--linkHoverColor);
  text-decoration: var(--linkHoverTextDecoration);
}

:root {
  --buttonFontFamily: 'Poppins', sans-serif;
  --buttonFontSize: 15px;
  --buttonFontWeight: inherit;
  --buttonLetterSpacing: 1px;
  --buttonFontColor: transparent;
  --buttonTextTransform: inherit;
  --buttonBorder: 1px solid transparent;
  --buttonBorderRadius: 5px;
}

button {
  font-family: var(--buttonFontFamily);
  font-size: var(--buttonFontSize);
  font-weight: var(--buttonFontWeight);
  color: var(--buttonFontColor);
  letter-spacing: var(--buttonLetterSpacing);
  text-transform: var(--buttonTextTransform);
  border: var(--buttonBorder);
  border-radius: var(--buttonBorderRadius);
}

:root {
  --buttonPrimarycolor: white;
  --buttonPrimarycolorhover: black;
  --buttonPrimaryOutline: black;
  --buttonPrimaryOutlinehover: black;
  --buttonPrimaryBorder: black;
  --buttonPrimaryBorderhover: black;
}

button.btn-primary {
  color: var(--buttonPrimarycolor);
  outline-color: var(--buttonPrimaryOutline);
  border-color: var(--buttonPrimaryBorder);
}

button.btn-primary:hover {
  color: var(--buttonPrimarycolorhover);
  outline-color: var(--buttonPrimaryOutlinehover);
  border-color: var(--buttonPrimaryBorderhover);
}

:root {
  --buttonSecondarycolor: white;
  --buttonSecondarycolorhover: black;
  --buttonSecondaryOutline: black;
  --buttonSecondaryOutlinehover: black;
  --buttonSecondaryBorder: black;
  --buttonSecondaryBorderhover: black;
}

button.btn-Secondary {
  color: var(--buttonSecondarycolor);
  outline-color: var(--buttonSecondaryOutline);
  border-color: var(--buttonSecondaryBorder);
}

button.btn-Secondary:hover {
  color: var(--buttonSecondarycolorhover);
  outline-color: var(--buttonSecondaryOutlinehover);
  border-color: var(--buttonSecondaryBorderhover);
}

:root {
  --otherBordercolor: black;
  --otherBorder2xcolor: black;
  --otherTextPrimary: black;
  --otherTextSecondary: black;
}
</style>
