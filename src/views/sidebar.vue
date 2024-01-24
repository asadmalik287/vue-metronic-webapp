<template>
    <div class="vfb-left-container position-relative">
      <ul class="nav nav-tabs leftSidebar_tabs" id="myTab" role="tablist">
        <li class="nav-item w-50" role="presentation">
          <button class="nav-link active w-100 text-dark is-first" id="home-tab" data-bs-toggle="tab" data-bs-target="#home"
            type="button" role="tab" aria-controls="home" aria-selected="true">Elements</button>
        </li>
        <li class="nav-item w-50" role="presentation">
          <button class="nav-link w-100 text-dark is-last" id="profile-tab" data-bs-toggle="tab" data-bs-target="#profile"
            type="button" role="tab" aria-controls="profile" aria-selected="false">Tree</button>
        </li>
  
      </ul>
      <div class="tab-content bg-white pb-5 h-100" id="myTabContent">
        <div class="tab-pane bg-white fade show active" id="home" role="tabpanel" aria-labelledby="home-tab">
          <div class="top-element-serach">
            <div class="vfb-elements-search-container">
                <form role="search"><input type="search" class="vfb-elements-search-input" placeholder="Search elements"
                        role="searchbox"></form><svg class="vfb-icon vfb-elements-search-icon" aria-hidden="true"
                    focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                    <path class="" fill="#b0bbcb"
                        d="M508.5 481.6l-129-129c-2.3-2.3-5.3-3.5-8.5-3.5h-10.3C395 312 416 262.5 416 208 416 93.1 322.9 0 208 0S0 93.1 0 208s93.1 208 208 208c54.5 0 104-21 141.1-55.2V371c0 3.2 1.3 6.2 3.5 8.5l129 129c4.7 4.7 12.3 4.7 17 0l9.9-9.9c4.7-4.7 4.7-12.3 0-17zM208 384c-97.3 0-176-78.7-176-176S110.7 32 208 32s176 78.7 176 176-78.7 176-176 176z">
                    </path><!--v-if-->
                </svg><!--v-if-->
            </div>
        </div>
        <div class="px-3 py-2">
          <ul class="nav nav-pills border mb-3 category_tabs" id="category-tab" role="tablist">
              <li class="nav-item" role="presentation">
                  <button class="nav-link active text-black tabFirst w-100" id="field-home-tab" data-bs-toggle="pill"
                      data-bs-target="#field-home" type="button" role="tab" aria-controls="pills-home"
                      aria-selected="true">Fields</button>
              </li>
              <li class="nav-item" role="presentation">
                  <button class="nav-link text-black tabCenter w-100" id="static-profile-tab" data-bs-toggle="pill"
                      data-bs-target="#static-profile" type="button" role="tab" aria-controls="pills-profile"
                      aria-selected="false">Static</button>
              </li>
              <li class="nav-item" role="presentation">
                  <button class="nav-link text-black tablast w-100" id="structure-contact-tab" data-bs-toggle="pill"
                      data-bs-target="#structure-contact" type="button" role="tab" aria-controls="pills-contact"
                      aria-selected="false">Structure</button>
              </li>
          </ul>
          <div class="tab-content" id="category-tabContent">
              <div class="tab-pane fade show active" id="field-home" role="tabpanel" aria-labelledby="pills-home-tab">
                  <div>
                      <div
                        class="vfb-element-container vfb-element-container-enabled d-flex cursor-pointer"
                        draggable="true"
                        title=""
                        tabindex="-1"
                        role="option"
                        data-id="text-field"
                        data-code="Text"
                        id="NewTextid"
                        ondrop="newboxclickfuc(this)"
                      >
                        <div class="vfb-element-icon-container">
                          <svg
                            class="vfb-icon vfb-element-icon"
                            aria-hidden="true"
                            focusable="false"
                            role="img"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 640 512"
                          >
                            <path
                              class=""
                              fill="currentColor"
                              d="M229.88 85.69A32 32 0 0 0 199.58 64h-47.16a32 32 0 0 0-30.3 21.69L.85 426.89A16 16 0 0 0 16 448h50.62a16 16 0 0 0 15.16-10.89L100.85 384h150.3l19.07 53.11A16 16 0 0 0 285.38 448H336a16 16 0 0 0 15.16-21.11zM129.58 304L176 174.74 222.42 304zM624 160h-32a16 16 0 0 0-16 16v1.81c-18.9-11-40.58-17.81-64-17.81a128.14 128.14 0 0 0-128 128v32a128.14 128.14 0 0 0 128 128c23.42 0 45.1-6.78 64-17.81V432a16 16 0 0 0 16 16h32a16 16 0 0 0 16-16V176a16 16 0 0 0-16-16zm-64 160a48 48 0 0 1-96 0v-32a48 48 0 0 1 96 0z"
                            ></path>
                          </svg>
                        </div>
                        <div id="vfb-text-field-container" class="vfb-element-text-container">
                          <div class="vfb-element-text-label">Text input</div>
                          <div class="vfb-element-text-description">Single line text input</div>
                        </div>
                      </div>
                      <!-- ------------------- -->
                      <div
                        class="vfb-element-container vfb-element-container-enabled d-flex cursor-pointer"
                        draggable="true"
                        title=""
                        tabindex="-1"
                        role="option"
                        data-code="multiple_select"
                      >
                        <div class="vfb-element-icon-container">
                          <svg
                            class="vfb-icon vfb-element-icon"
                            aria-hidden="true"
                            focusable="false"
                            role="img"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 448 512"
                          >
                            <path
                              class=""
                              fill="currentColor"
                              d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-32 252c0 6.6-5.4 12-12 12h-92v92c0 6.6-5.4 12-12 12h-56c-6.6 0-12-5.4-12-12v-92H92c-6.6 0-12-5.4-12-12v-56c0-6.6 5.4-12 12-12h92v-92c0-6.6 5.4-12 12-12h56c6.6 0 12 5.4 12 12v92h92c6.6 0 12 5.4 12 12v56z"
                            ></path>
                            <!--v-if-->
                          </svg>
                        </div>
                        <div class="vfb-element-text-container">
                          <div class="vfb-element-text-label">Multiselect</div>
                          <div class="vfb-element-text-description">Multiselect input</div>
                        </div>
                      </div>
                  
                      <!-- ------------------- -->
                      <!-- ------------------- -->
                      <div
                        class="vfb-element-container vfb-element-container-enabled d-flex cursor-pointer"
                        draggable="true"
                        title=""
                        tabindex="-1"
                        role="option"
                        data-code="upload"
                      >
                        <div class="vfb-element-icon-container">
                          <svg
                            class="vfb-icon vfb-element-icon"
                            aria-hidden="true"
                            focusable="false"
                            role="img"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 576 512"
                          >
                            <path
                              class=""
                              fill="currentColor"
                              d="M480 416v16c0 26.51-21.49 48-48 48H48c-26.51 0-48-21.49-48-48V176c0-26.51 21.49-48 48-48h16v208c0 44.112 35.888 80 80 80h336zm96-80V80c0-26.51-21.49-48-48-48H144c-26.51 0-48 21.49-48 48v256c0 26.51 21.49 48 48 48h384c26.51 0 48-21.49 48-48zM256 128c0 26.51-21.49 48-48 48s-48-21.49-48-48 21.49-48 48-48 48 21.49 48 48zm-96 144l55.515-55.515c4.686-4.686 12.284-4.686 16.971 0L272 256l135.515-135.515c4.686-4.686 12.284-4.686 16.971 0L512 208v112H160v-48z"
                            ></path>
                            <!--v-if-->
                          </svg>
                        </div>
                        <div class="vfb-element-text-container">
                          <div class="vfb-element-text-label">Multi-image upload</div>
                          <div class="vfb-element-text-description">Multi-file upload with images only</div>
                        </div>
                      </div>
                   
                    </div>
              </div>
              <div class="tab-pane fade" id="static-profile" role="tabpanel" aria-labelledby="static-profile-tab">
                  <div>
                      <div class="vfb-element-container vfb-element-container-enabled d-flex cursor-pointer" draggable="true" title="" tabindex="-1"  data-code="ImageUpload"
                          role="option">
                          <div class="vfb-element-icon-container"><svg class="vfb-icon vfb-element-icon" aria-hidden="true"
                                  focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                                  <path class="" fill="currentColor"
                                      d="M128 192a32 32 0 1 0-32-32 32 32 0 0 0 32 32zM416 32H32A32 32 0 0 0 0 64v384a32 32 0 0 0 32 32h384a32 32 0 0 0 32-32V64a32 32 0 0 0-32-32zm-32 320H64V96h320zM268.8 209.07a16 16 0 0 0-25.6 0l-49.32 65.75L173.31 244a16 16 0 0 0-26.62 0L96 320h256z">
                                  </path><!--v-if-->
                              </svg></div>
                          <div class="vfb-element-text-container">
                          <div class="vfb-element-text-label">Image</div>
                          <div class="vfb-element-text-description">HTML &lt;img&gt; tag</div>
                      </div>
                  </div>
              </div>
              </div>
              <div class="tab-pane fade" id="structure-contact" role="tabpanel" aria-labelledby="structure-contact-tab">
                  <div>
                      <div class="vfb-element-container vfb-element-container-enabled d-flex cursor-pointer" draggable="true" title="" tabindex="-1"  data-code="VueTabs"
                          role="option">
                          <div class="vfb-element-icon-container"><svg class="vfb-icon vfb-element-icon" aria-hidden="true"
                                  focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                                  <path class="" fill="currentColor"
                                      d="M464 128H272l-64-64H48C21.49 64 0 85.49 0 112v288c0 26.51 21.49 48 48 48h416c26.51 0 48-21.49 48-48V176c0-26.51-21.49-48-48-48z">
                                  </path><!--v-if-->
                              </svg></div>
                          <div class="vfb-element-text-container">
                          <div class="vfb-element-text-label">Tabs</div>
                          <div class="vfb-element-text-description">Break forms into tabs</div>
                      </div>
                  </div>
              </div>
              </div>
          </div>
      </div>
        </div>
        <div class="tab-pane bg-white fade" id="profile" role="tabpanel" aria-labelledby="profile-tab">
          <Search />
        </div>
      </div>
      <div>
      
        <!-- ------------- -->
        <!-- ------------- -->
        <div class="position-absolute vfb-bottom-left-tools">
            <div class=" vfb-bottom-left-tools-container">
                <div class="vfb-tool vfb-tool-toggle-left">
                    <div class="vfb-tool-item vfb-tool-item-single vfb-tool-item-hoverable" tabindex="0" role="button"
                        aria-label="Close left panel"><svg class="vfb-icon" aria-hidden="true" focusable="false" role="img"
                            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                            <path class="" fill="currentColor"
                                d="M247.9 412.5l-148.4-148c-4.7-4.7-4.7-12.3 0-17l148.4-148c4.7-4.7 12.3-4.7 17 0l19.6 19.6c4.8 4.8 4.7 12.5-.2 17.1L187.2 230H436c6.6 0 12 5.4 12 12v28c0 6.6-5.4 12-12 12H187.2l97.1 93.7c4.8 4.7 4.9 12.4.2 17.1l-19.6 19.6c-4.7 4.8-12.3 4.8-17 .1zM52 436V76c0-6.6-5.4-12-12-12H12C5.4 64 0 69.4 0 76v360c0 6.6 5.4 12 12 12h28c6.6 0 12-5.4 12-12z">
                            </path><!--v-if-->
                    </svg>
                    <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Close panel</div>
                </div>
            </div>
            <div class="vfb-tool vfb-tool-clear">
                <div class="vfb-tool-item vfb-tool-item-single vfb-tool-item-hoverable" tabindex="0" role="button"
                    aria-label="Clear form"><svg class="vfb-icon" aria-hidden="true" focusable="false" role="img"
                        xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                        <path class="" fill="currentColor"
                            d="M268 416h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12zM432 80h-82.41l-34-56.7A48 48 0 0 0 274.41 0H173.59a48 48 0 0 0-41.16 23.3L98.41 80H16A16 16 0 0 0 0 96v16a16 16 0 0 0 16 16h16v336a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V128h16a16 16 0 0 0 16-16V96a16 16 0 0 0-16-16zM171.84 50.91A6 6 0 0 1 177 48h94a6 6 0 0 1 5.15 2.91L293.61 80H154.39zM368 464H80V128h288zm-212-48h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12z">
                        </path><!--v-if-->
                    </svg>
                    <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Clear form</div>
                </div>
            </div>
        </div>
        </div>
        <div class="position-absolute vfb-top-left-tools">
    <div class="vfb-top-left-tools-container sdsd">
      <div class="vfb-tool vfb-tool-view">
        <div
          @click="showTool($event, 'editor')"
          class="vfb-tool-item vfb-tool-item-active-primary vfb-tool-item-first"
          tabindex="0"
          role="button"
          aria-roledescription="View"
          aria-label="Editor"
        >
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M402.3 344.9l32-32c5-5 13.7-1.5 13.7 5.7V464c0 26.5-21.5 48-48 48H48c-26.5 0-48-21.5-48-48V112c0-26.5 21.5-48 48-48h273.5c7.1 0 10.7 8.6 5.7 13.7l-32 32c-1.5 1.5-3.5 2.3-5.7 2.3H48v352h352V350.5c0-2.1.8-4.1 2.3-5.6zm156.6-201.8L296.3 405.7l-90.4 10c-26.2 2.9-48.5-19.2-45.6-45.6l10-90.4L432.9 17.1c22.9-22.9 59.9-22.9 82.7 0l43.2 43.2c22.9 22.9 22.9 60 .1 82.8zM460.1 174L402 115.9 216.2 301.8l-7.3 65.3 65.3-7.3L460.1 174zm64.8-79.7l-43.2-43.2c-4.1-4.1-10.8-4.1-14.8 0L436 82l58.1 58.1 30.9-30.9c4-4.2 4-10.8-.1-14.9z"
            ></path>
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Editor</div>
        </div>
        <div
          @click="showTool($event, 'array')"
          class="vfb-tool-item"
          tabindex="0"
          role="button"
          aria-roledescription="View"
          aria-label="Preview"
        >
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M288 144a110.94 110.94 0 0 0-31.24 5 55.4 55.4 0 0 1 7.24 27 56 56 0 0 1-56 56 55.4 55.4 0 0 1-27-7.24A111.71 111.71 0 1 0 288 144zm284.52 97.4C518.29 135.59 410.93 64 288 64S57.68 135.64 3.48 241.41a32.35 32.35 0 0 0 0 29.19C57.71 376.41 165.07 448 288 448s230.32-71.64 284.52-177.41a32.35 32.35 0 0 0 0-29.19zM288 400c-98.65 0-189.09-55-237.93-144C98.91 167 189.34 112 288 112s189.09 55 237.93 144C477.1 345 386.66 400 288 400z"
            ></path>
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Preview</div>
        </div>
        <!-- <div
          class="vfb-tool-item vfb-tool-item-last"
          tabindex="0"
          role="button"
          aria-roledescription="View"
          aria-label="Code"
        >
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M234.8 511.7L196 500.4c-4.2-1.2-6.7-5.7-5.5-9.9L331.3 5.8c1.2-4.2 5.7-6.7 9.9-5.5L380 11.6c4.2 1.2 6.7 5.7 5.5 9.9L244.7 506.2c-1.2 4.3-5.6 6.7-9.9 5.5zm-83.2-121.1l27.2-29c3.1-3.3 2.8-8.5-.5-11.5L72.2 256l106.1-94.1c3.4-3 3.6-8.2.5-11.5l-27.2-29c-3-3.2-8.1-3.4-11.3-.4L2.5 250.2c-3.4 3.2-3.4 8.5 0 11.7L140.3 391c3.2 3 8.2 2.8 11.3-.4zm284.1.4l137.7-129.1c3.4-3.2 3.4-8.5 0-11.7L435.7 121c-3.2-3-8.3-2.9-11.3.4l-27.2 29c-3.1 3.3-2.8 8.5.5 11.5L503.8 256l-106.1 94.1c-3.4 3-3.6 8.2-.5 11.5l27.2 29c3.1 3.2 8.1 3.4 11.3.4z"
            ></path>
           
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Code</div>
      </div>  -->
      </div>
      <!-- <div class="vfb-tool vfb-tool-device">
        <div
          class="vfb-tool-item vfb-tool-item vfb-tool-item-first vfb-tool-item-active"
          tabindex="0"
          role="button"
          aria-roledescription="Device"
          aria-label="Default"
        >
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 320 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M272 0H48C21.5 0 0 21.5 0 48v416c0 26.5 21.5 48 48 48h224c26.5 0 48-21.5 48-48V48c0-26.5-21.5-48-48-48zM160 480c-17.7 0-32-14.3-32-32s14.3-32 32-32 32 14.3 32 32-14.3 32-32 32zm112-108c0 6.6-5.4 12-12 12H60c-6.6 0-12-5.4-12-12V60c0-6.6 5.4-12 12-12h200c6.6 0 12 5.4 12 12v312z"
            ></path>
            
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Default</div>
        </div>
        <div
          class="vfb-tool-item vfb-tool-item"
          tabindex="0"
          role="button"
          aria-roledescription="Device"
          aria-label="Tablet (>=640px)"
        >
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 448 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M400 0H48C21.5 0 0 21.5 0 48v416c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V48c0-26.5-21.5-48-48-48zM224 480c-17.7 0-32-14.3-32-32s14.3-32 32-32 32 14.3 32 32-14.3 32-32 32zm176-108c0 6.6-5.4 12-12 12H60c-6.6 0-12-5.4-12-12V60c0-6.6 5.4-12 12-12h328c6.6 0 12 5.4 12 12v312z"
            ></path>
            
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Tablet (&gt;=640px)</div>
        </div>
        <div
          class="vfb-tool-item vfb-tool-item vfb-tool-item-last"
          tabindex="0"
          role="button"
          aria-roledescription="Device"
          aria-label="Desktop (>=1024px)"
        >
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M528 0H48C21.5 0 0 21.5 0 48v288c0 26.5 21.5 48 48 48h480c26.5 0 48-21.5 48-48V48c0-26.5-21.5-48-48-48zm-6 336H54c-3.3 0-6-2.7-6-6V54c0-3.3 2.7-6 6-6h468c3.3 0 6 2.7 6 6v276c0 3.3-2.7 6-6 6zm-42 152c0 13.3-10.7 24-24 24H120c-13.3 0-24-10.7-24-24s10.7-24 24-24h98.7l18.6-55.8c1.6-4.9 6.2-8.2 11.4-8.2h78.7c5.2 0 9.8 3.3 11.4 8.2l18.6 55.8H456c13.3 0 24 10.7 24 24z"
            ></path>
            
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Desktop (&gt;=1024px)</div>
        </div>
      </div>  -->
      <!-- <div class="vfb-tool vfb-tool-dark-mode">
        <div class="vfb-tool-item vfb-tool-item vfb-tool-item-first vfb-tool-item-active">
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 512 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M494.2 221.9l-59.8-40.5 13.7-71c2.6-13.2-1.6-26.8-11.1-36.4-9.6-9.5-23.2-13.7-36.2-11.1l-70.9 13.7-40.4-59.9c-15.1-22.3-51.9-22.3-67 0l-40.4 59.9-70.8-13.7C98 60.4 84.5 64.5 75 74.1c-9.5 9.6-13.7 23.1-11.1 36.3l13.7 71-59.8 40.5C6.6 229.5 0 242 0 255.5s6.7 26 17.8 33.5l59.8 40.5-13.7 71c-2.6 13.2 1.6 26.8 11.1 36.3 9.5 9.5 22.9 13.7 36.3 11.1l70.8-13.7 40.4 59.9C230 505.3 242.6 512 256 512s26-6.7 33.5-17.8l40.4-59.9 70.9 13.7c13.4 2.7 26.8-1.6 36.3-11.1 9.5-9.5 13.6-23.1 11.1-36.3l-13.7-71 59.8-40.5c11.1-7.5 17.8-20.1 17.8-33.5-.1-13.6-6.7-26.1-17.9-33.7zm-112.9 85.6l17.6 91.2-91-17.6L256 458l-51.9-77-90.9 17.6 17.6-91.2-76.8-52 76.8-52-17.6-91.2 91 17.6L256 53l51.9 76.9 91-17.6-17.6 91.1 76.8 52-76.8 52.1zM256 152c-57.3 0-104 46.7-104 104s46.7 104 104 104 104-46.7 104-104-46.7-104-104-104zm0 160c-30.9 0-56-25.1-56-56s25.1-56 56-56 56 25.1 56 56-25.1 56-56 56z"
            ></path>
            
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">Light preview</div>
        </div>
        <div
          class="vfb-tool-item vfb-tool-item vfb-tool-item-last vfb-tool-item-disabled"
        >
          <svg
            class="vfb-icon"
            aria-hidden="true"
            focusable="false"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 512 512"
          >
            <path
              class=""
              fill="currentColor"
              d="M279.135 512c78.756 0 150.982-35.804 198.844-94.775 28.27-34.831-2.558-85.722-46.249-77.401-82.348 15.683-158.272-47.268-158.272-130.792 0-48.424 26.06-92.292 67.434-115.836 38.745-22.05 28.999-80.788-15.022-88.919A257.936 257.936 0 0 0 279.135 0c-141.36 0-256 114.575-256 256 0 141.36 114.576 256 256 256zm0-464c12.985 0 25.689 1.201 38.016 3.478-54.76 31.163-91.693 90.042-91.693 157.554 0 113.848 103.641 199.2 215.252 177.944C402.574 433.964 344.366 464 279.135 464c-114.875 0-208-93.125-208-208s93.125-208 208-208z"
            ></path>
            
          </svg>
          <div class="vfb-tool-tooltip vfb-tool-tooltip-right">
            Dark preview - coming soon
          </div>
        </div>
      </div>  -->
    </div>
  </div>
  </div>
    </div>
  
  </template>
  <script>
  // import Search from './sidebarcomponents/Search.vue'
  // import Category from './sidebarcomponents/Category.vue'
  // import LeftTool from './sidebarcomponents/LeftTool.vue';
  export default {
    name: 'SidebarComponent',
    components: {
      // Search,
      // Category,
      // LeftTool ,
    },
    methods: {
        showTool(event, type) {
      // Select all elements with the class "vfb-tool-item"
      const toolItems = document.querySelectorAll(".vfb-tool-item");
      const toolItemsaction = document.querySelectorAll(".vfb-action");
      // Iterate over the NodeList
      toolItems.forEach((toolItem, index) => {
        // Do something with each tool item
        toolItem.classList.remove("vfb-tool-item-active-primary");
      });
      event.currentTarget.classList.add("vfb-tool-item-active-primary");

      if (type == "array") {
        // Iterate over the NodeList
        toolItemsaction.forEach((toolItem, index) => {
          // Do something with each tool item
          toolItem.style.display = "none";
        });
        event.currentTarget.classList.add("vfb-tool-item-active-primary");
        document.getElementById("vfbmodelarray").style.right = "0px";
      } else {
        toolItemsaction.forEach((toolItem, index) => {
          // Do something with each tool item
          toolItem.style.display = "";
        });
        document.getElementById("vfbmodelarray").style.right = "-400px";
      }
    },
    }
  };
  </script>
    
  <style scoped>
  /* Add any custom styling for your Navbar component here */
  </style>
    