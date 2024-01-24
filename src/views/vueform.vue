<template>
  <sidebar/>
 
  <div class="vfb-preview-container">
    <div
      class="vfb-preview-wrapper vfb-preview-wrapper-preview"
      tabindex="-1"
      aria-label="Form elements"
      aria-describedby="vfb-preview-description"
    >
      <span id="vfb-preview-description" class="vfb-util-assistive-text"
        >Use up and down arrows to navigate.</span
      >
      <form
        id="drop-container"
        ref="dropContainer"
        class="vfb-preview-form"
        @dragstart="handleDragAbleStart"
        @dragover="handleDragAbleOver"
        @drop="handleDropAble"
      >
        <div class="grid grid-cols-12 form-gap-x-gutter form-gap-y-gutter"></div>
        <div
          id="remv-after-dropped"
          class="vfb-preview-empty-container vfb-preview-empty-container-inactive"
        >
          <div class="vfb-preview-empty-icon-container">
            <!-- Replace the placeholder SVG with your actual SVG icon -->
            <svg
              class="vfb-icon vfb-preview-empty-icon"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 494 492"
            >
              <!-- Your SVG path data here -->
              <path
                class=""
                fill="currentColor"
                d="M357.464858,88.3197621 C356.007587,89.7731912 354.100792,90.8076945 351.91325,91.184 C346.643273,92.0696 340.55125,93.7568706 333.840762,96.1647765 C332.688738,96.5767059 331.515488,96.7619294 330.3625,96.7619294 C326.143238,96.7619294 322.191238,94.1485412 320.66775,89.9501412 C318.7535,84.5998824 321.53225,78.7132471 326.884238,76.7790118 C334.747715,73.9591765 342.012988,71.9834588 348.476477,70.8721176 C348.961603,70.7954549 349.44457,70.7532564 349.922738,70.743781 C349.9189,70.4238759 349.916988,70.1032877 349.916988,69.782 C349.916988,65.1301882 350.349238,60.5825647 351.213738,56.1574588 C352.28375,50.6007529 357.635738,46.9580235 363.27525,48.0076235 C368.853012,49.0774824 372.496262,54.4692235 371.42625,60.0674118 C370.829012,63.2364706 370.5,66.4884941 370.5,69.8225176 C370.5,72.3336471 370.664988,74.7618118 371.014262,77.1282353 C371.817012,82.7466824 367.926762,87.9744235 362.28725,88.7770588 C361.79325,88.8388 361.29925,88.8802824 360.80525,88.8802824 C359.644864,88.8802824 358.519365,88.6841668 357.464858,88.3197621 Z M112.892398,288.353484 C131.722318,301.360374 144.08338,323.0923 144.083977,347.657812 C144.083977,387.378612 111.768465,419.689506 72.0419883,419.689506 C32.3155117,419.689506 -1.84741111e-13,387.377647 -1.84741111e-13,347.657812 C-1.84741111e-13,307.937976 32.3155117,275.626118 72.0419883,275.626118 C79.7380815,275.626118 87.1560627,276.838846 94.1148474,279.083224 C95.7814215,273.702036 98.1796971,268.00261 101.27,262.064282 C103.904988,257.021765 110.120512,255.066306 115.16375,257.700918 C120.206988,260.335529 122.1415,266.550165 119.526773,271.592682 C116.337,277.6848 114.114,283.323506 112.899262,288.324541 C112.896985,288.334194 112.894696,288.343841 112.892394,288.353481 Z M399.378738,300.220329 C420.57925,321.438071 432.25,349.592047 432.25,379.557741 C432.25,441.401176 381.92375,491.720235 320.069547,491.719271 L195.540059,491.719271 C189.859059,491.719271 185.24807,487.108941 185.24807,481.428753 C185.24807,453.069294 208.34257,429.978094 236.706082,429.978094 L253.028344,429.978094 L174.338582,351.299576 C168.265855,345.228682 164.911094,337.160847 164.911094,328.578824 C164.911094,319.9968 168.26682,311.928965 174.338582,305.858071 C186.462809,293.7568 207.621832,293.715318 219.76632,305.858071 L238.209309,324.298424 C239.774285,320.779176 241.976059,317.485671 244.858047,314.625318 C252.000785,307.484565 262.231023,304.129318 272.069535,305.529106 C273.242785,299.437953 276.166262,293.613059 280.879523,288.900471 C289.874762,279.907482 302.882785,277.354871 314.162773,281.286047 C315.666,276.552235 318.300023,272.086612 322.046512,268.3204 C334.5615,255.8072 354.959262,255.8072 367.47425,268.3204 L399.378738,300.220329 Z M320.070512,471.140165 C370.582012,471.140165 411.666988,430.062024 411.666023,379.556776 C411.666023,355.107271 402.136262,332.098071 384.846262,314.810541 L352.941773,282.910612 C348.434023,278.403506 341.127262,278.403506 336.619512,282.910612 C332.111762,287.417718 332.111762,294.723435 336.619512,299.230541 C338.637,301.247741 339.625,303.881388 339.625,306.516 C339.625,309.150612 338.615773,311.784259 336.619512,313.801459 C332.605762,317.814635 326.080523,317.814635 322.066773,313.801459 L311.774785,303.510941 C307.267035,299.003835 299.960273,299.003835 295.452523,303.510941 C293.270047,305.692141 292.076535,308.593976 292.076535,311.660776 C292.076535,314.727576 293.271012,317.649671 295.452523,319.810612 L305.744512,330.101129 C307.741738,332.098071 308.75,334.731718 308.75,337.366329 C308.75,340.000941 307.740773,342.634588 305.744512,344.651788 C301.730762,348.664965 295.205523,348.664965 291.191773,344.651788 L275.754273,329.216494 C271.39125,324.853129 263.796,324.853129 259.432012,329.216494 C257.249535,331.397694 256.056023,334.299529 256.056023,337.366329 C256.056023,340.433129 257.2505,343.355224 259.432012,345.516165 L285.1615,371.241976 C287.158727,373.259176 288.166988,375.892824 288.166988,378.527435 C288.166988,381.162047 287.157762,383.795694 285.1615,385.812894 C281.14775,389.826071 274.622512,389.826071 270.608762,385.812894 L205.215512,320.428988 C200.852488,316.065624 193.257238,316.086847 188.89325,320.428988 C186.711738,322.610188 185.497,325.512024 185.497,328.578824 C185.497,331.645624 186.711738,334.567718 188.89325,336.728659 L285.141238,432.962894 C288.084977,435.906212 288.969738,440.331318 287.364238,444.179529 C285.779,448.027741 282.01225,450.538871 277.854738,450.538871 L236.68775,450.538871 C223.288,450.560094 211.843988,459.162376 207.583238,471.140165 L320.070512,471.140165 Z M72.0419883,399.108471 C100.4055,399.108471 123.5,376.017271 123.5,347.657812 C123.5,319.298353 100.4055,296.207153 72.0419883,296.207153 C43.6784766,296.207153 20.5839766,319.298353 20.5839766,347.657812 C20.5839766,376.017271 43.6784766,399.108471 72.0419883,399.108471 Z M400.57225,116.622329 C405.738988,118.988753 408.002512,125.080871 405.655047,130.267129 C403.926047,134.0536 400.179559,136.276282 396.269047,136.276282 C394.848797,136.276282 393.388023,135.967576 391.988035,135.350165 C384.701535,132.016141 378.032535,127.509035 372.207773,121.932071 C368.09175,118.021153 367.947023,111.497812 371.878762,107.381412 C375.8105,103.265976 382.335738,103.101012 386.4315,107.052447 C390.589012,111.024141 395.343762,114.255906 400.57225,116.622329 Z M395.158512,2.95682353 C400.428488,0.837364706 406.418238,3.40927059 408.537035,8.65823529 C410.657762,13.9274588 408.104785,19.9366118 402.835773,22.0358118 C397.505012,24.1755294 392.6065,27.1805882 388.242512,30.9468 C386.328262,32.6138118 383.920012,33.4367059 381.532023,33.4367059 C378.650035,33.4367059 375.789273,32.2221412 373.751523,29.8759765 C370.026262,25.5946118 370.5,19.0915294 374.781012,15.3870588 C380.852773,10.1188 387.72825,5.94065882 395.158512,2.95682353 Z M463.783988,11.1684 C468.415238,14.4821647 469.48525,20.9032471 466.171977,25.5126118 C464.134227,28.3121882 460.984977,29.8142353 457.773977,29.8142353 C455.694738,29.8142353 453.6155,29.1968235 451.804488,27.9002588 C447.132715,24.5662353 441.965977,22.0551059 436.470227,20.4498353 C431.015965,18.8445647 427.886977,13.1441176 429.492477,7.66941176 C431.097977,2.21592941 436.840727,-0.892352941 442.274727,0.692658824 C449.993477,2.95682353 457.238488,6.47607059 463.783988,11.1684 Z M449.787,113.103082 C454.583238,110.057506 460.943488,111.394588 464.010727,116.189176 C467.077965,120.963506 465.719465,127.343106 460.923227,130.409906 C454.17125,134.753012 446.782477,137.922071 438.960488,139.836047 C438.136512,140.042494 437.3135,140.124494 436.51075,140.124494 C431.8795,140.124494 427.659273,136.975694 426.527512,132.263106 C425.190238,126.727624 428.586488,121.170918 434.1025,119.832871 C439.680262,118.474565 444.9705,116.2104 449.787,113.103082 Z M491.118012,49.5299294 C493.032262,56.1159765 494,62.9489882 494,69.8427765 C494,77.9106118 492.682988,85.8337412 490.068262,93.3873882 C488.586262,97.6272706 484.592773,100.3024 480.332023,100.3024 C479.220523,100.3024 478.087797,100.117176 476.956035,99.7467294 C471.583785,97.8944941 468.743285,92.0290824 470.595785,86.6576 C472.469512,81.2648941 473.416023,75.5847059 473.416023,69.8225176 C473.416023,64.8832235 472.736773,60.0056706 471.358012,55.3336 C469.752512,49.8801176 472.8815,44.1787059 478.335762,42.5531765 C483.851773,41.0096471 489.512512,44.0967059 491.118012,49.5299294 Z M185.167988,166.776424 C189.490488,163.113435 195.974238,163.565882 199.679238,167.908024 C203.384238,172.209647 202.869977,178.712729 198.547477,182.4172 C193.401965,186.862565 188.317238,191.349412 183.418727,195.876776 C181.422465,197.688494 178.931238,198.573129 176.440977,198.573129 C173.662227,198.573129 170.883477,197.461788 168.865988,195.239106 C165.017227,191.060965 165.30475,184.536659 169.483488,180.688447 C174.588477,175.996118 179.816,171.345271 185.167988,166.776424 Z M139.658238,210.345435 C143.527262,206.167294 150.011012,205.920329 154.210012,209.769506 C158.387785,213.638941 158.634785,220.142024 154.786023,224.320165 C150.093023,229.382941 145.708773,234.404235 141.633273,239.385012 C139.575262,241.854659 136.631523,243.151224 133.647262,243.151224 C131.362512,243.151224 129.037238,242.389106 127.14325,240.825318 C122.738738,237.223106 122.100977,230.740282 125.702738,226.3364 C130.025238,221.068141 134.697977,215.716918 139.658238,210.345435 Z M288.06375,94.6627294 C293.0655,91.9461176 299.30225,93.8195765 302.020215,98.7993882 C304.737215,103.800424 302.884715,110.036282 297.882965,112.752894 C292.180738,115.839953 286.355977,119.194235 280.427977,122.775224 C278.740465,123.783341 276.908227,124.277271 275.097215,124.277271 C271.617988,124.277271 268.221738,122.508 266.287227,119.317718 C263.343488,114.460424 264.9075,108.142565 269.765488,105.178988 C275.96075,101.412776 282.074,97.8935294 288.06375,94.6627294 Z M234.71175,128.188188 C239.363262,124.895647 245.765,126.006988 249.057047,130.656871 C252.350059,135.287459 251.238559,141.708541 246.587047,145.001082 C241.112523,148.870518 235.637035,152.862471 230.203035,156.978871 C228.350535,158.378659 226.169023,159.057812 224.007773,159.057812 C220.900012,159.057812 217.812512,157.658988 215.795023,154.962635 C212.35825,150.435271 213.263273,143.972706 217.812512,140.556682 C223.4115,136.317765 229.051012,132.201365 234.71175,128.188188 Z"
              ></path>
            </svg>
          </div>
          <div class="vfb-preview-empty-title">Drag elements here</div>
          <div class="vfb-preview-empty-description">
            Grab an element from the left and drop it here
          </div>
        </div>
      </form>
    </div>
  </div>
  <!-- <  ------------------------------ > -->
  <section>
    <div class="vfb-right-container" style="right: -500px" id="rightMenu">
      <div class="position-relative h-100">
        <div class="vfb-panels-wrapper-multiselect">
          <div class="vfb-config-panel-header-container">
            <div class="vfb-config-panel-header">
              <div class="vfb-config-panel-header-wrapper-left">
                <span
                  class="vfb-config-panel-header-close"
                  tabindex="0"
                  @click="textClose"
                  role="button"
                  aria-label="Close config panel"
                  ><svg
                    class="vfb-icon vfb-config-panel-header-close-icon"
                    aria-hidden="true"
                    focusable="false"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 320 512"
                  >
                    <path
                      class=""
                      fill="currentColor"
                      d="M207.6 256l107.72-107.72c6.23-6.23 6.23-16.34 0-22.58l-25.03-25.03c-6.23-6.23-16.34-6.23-22.58 0L160 208.4 52.28 100.68c-6.23-6.23-16.34-6.23-22.58 0L4.68 125.7c-6.23 6.23-6.23 16.34 0 22.58L112.4 256 4.68 363.72c-6.23 6.23-6.23 16.34 0 22.58l25.03 25.03c6.23 6.23 16.34 6.23 22.58 0L160 303.6l107.72 107.72c6.23 6.23 16.34 6.23 22.58 0l25.03-25.03c6.23-6.23 6.23-16.34 0-22.58L207.6 256z"
                    ></path>
                    <!--v-if-->
                  </svg></span
                ><span class="vfb-config-panel-header-label">{{
                  targetElementData?.identification
                }}</span>
              </div>
              <div class="vfb-config-panel-header-wrapper-right">
                <!-- Clone -->
                <div
                  @click="cloneTextElement($event)"
                  class="vfb-config-panel-header-clone"
                  tabindex="0"
                  role="button"
                  aria-label="Clone"
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
                      d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zm-80 464c0 8.82-7.18 16-16 16H48c-8.82 0-16-7.18-16-16V144c0-8.82 7.18-16 16-16h48v240c0 26.51 21.49 48 48 48h240v48zm96-96c0 8.82-7.18 16-16 16H144c-8.82 0-16-7.18-16-16V48c0-8.82 7.18-16 16-16h320c8.82 0 16 7.18 16 16v320z"
                    ></path>
                    <!--v-if-->
                  </svg>
                </div>
                <!-- Remove -->
                <div
                  @click="deleteTextElement($event)"
                  class="vfb-config-panel-header-remove"
                  tabindex="0"
                  role="button"
                  aria-label="Remove"
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
                      d="M296 432h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zm-160 0h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zM440 64H336l-33.6-44.8A48 48 0 0 0 264 0h-80a48 48 0 0 0-38.4 19.2L112 64H8a8 8 0 0 0-8 8v16a8 8 0 0 0 8 8h24v368a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V96h24a8 8 0 0 0 8-8V72a8 8 0 0 0-8-8zM171.2 38.4A16.1 16.1 0 0 1 184 32h80a16.1 16.1 0 0 1 12.8 6.4L296 64H152zM384 464a16 16 0 0 1-16 16H80a16 16 0 0 1-16-16V96h320zm-168-32h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8z"
                    ></path>
                    <!--v-if-->
                  </svg>
                </div>
                <div
                  class="vfb-config-panel-header-collapse vv-vfb-icon-plus"
                  tabindex="0"
                  role="button"
                  aria-label="Expand all"
                  @click="ColapsToggleExpand"
                >
                  <svg
                    class="vfb-icon vfb-config-panel-header-collapse-icon-open"
                    aria-hidden="true"
                    focusable="false"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      class=""
                      fill="currentColor"
                      d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 206h-98v-98c0-6.6-5.4-12-12-12h-12c-6.6 0-12 5.4-12 12v98h-98c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h98v98c0 6.6 5.4 12 12 12h12c6.6 0 12-5.4 12-12v-98h98c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12z"
                    ></path>
                    <!--v-if-->
                  </svg>
                </div>
                <div
                  class="vfb-config-panel-header-collapse d-none vv-vfb-icon-close"
                  tabindex="0"
                  role="button"
                  aria-label="Collapse all"
                  @click="ColapsToggleClose"
                >
                  <svg
                    class="vfb-icon vfb-config-panel-header-collapse-icon-close"
                    aria-hidden="true"
                    focusable="false"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                  >
                    <path
                      class=""
                      fill="currentColor"
                      d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 242c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12H108c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h232z"
                    ></path>
                    <!--v-if-->
                  </svg>
                </div>
              </div>
            </div>
          </div>
          <div class="vfb-faqs">
            <div class="vfb-faqs-item">
              <div
                @click="handleClick"
                class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
              >
                <span class="medium text-black">Properties</span>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    fill="#94a3b8"
                    d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-close d-none"
                  aria-hidden="true"
                  focusable="false"
                  fill="#94a3b8"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div class="vfb-faqs-body bg-white" style="display: none">
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black">Name</span
                    ><input
                      type="text"
                      :value="targetElementData?.name"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'name')"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Input Field</span
                    >
                    <select
                      class="form-p-input-sm bg-input w-full transition-input duration-200 border-solid form-border-width-input form-shadow-input form-py-input-sm form-pl-input-sm form-pr-select-no-clear-sm form-radius-input-sm form-text-sm form-min-h-input-height-inner-sm with-floating:form-p-input-floating-sm rtl:form-pr-input-sm rtl:form-pl-select-no-clear-sm form-bg-input-success form-color-input-success form-border-color-input-success hover:form-shadow-input-hover focused:form-shadow-input-focus focused:form-ring focused-hover:form-shadow-input-hover"
                      name="inputType"
                      id="properties.inputType"
                      aria-labelledby="properties.inputType__label"
                      aria-describedby="properties.inputType__description properties.inputType__info"
                      aria-invalid="false"
                      aria-errormessage="properties.inputType__error"
                      aria-disabled="false"
                      aria-busy="false"
                      @change="setElementAttribute($event, 'type')"
                      :value="targetElementData?.type"
                    >
                      <option value="" disabled selected>Select type</option>
                      <option value="text">text</option>
                      <option value="color">color</option>
                      <option value="date">date</option>
                      <option value="datetime">datetime</option>
                      <option value="email">email</option>
                      <option value="month">month</option>
                      <option value="number">number</option>
                      <option value="password">password</option>
                      <option value="search">search</option>
                      <option value="tel">tel</option>
                      <option value="text">text</option>
                      <option value="time">time</option>
                      <option value="url">url</option>
                      <option value="week">week</option>
                    </select>
                  </div>
                </div>
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">Label</span
                    ><input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementLabel($event)"
                      :value="targetElementData?.label"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Tooltip</span
                    >
                    <input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setLabelTooltip($event)"
                      :value="targetElementData?.title"
                    />
                  </div>
                </div>
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Placeholder</span
                    >
                    <input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'placeholder')"
                      :value="targetElementData?.placeholder"
                    />
                  </div>

                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                    :class="{
                      //   'd-none': targetElementData?.autoFloat == 'default',
                      //  'd-flex': targetElementData?.autoFloat == 'off',
                    }"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Floating</span
                    >
                    <input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'floating')"
                      :value="targetElementData?.floating"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="vfb-faqs">
            <div class="vfb-faqs-item">
              <div
                @click="handleClick"
                class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
              >
                <span class="medium text-black">Data</span>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    fill="#94a3b8"
                    d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-close d-none"
                  aria-hidden="true"
                  focusable="false"
                  fill="#94a3b8"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div class="vfb-faqs-body bg-white" style="display: none">
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black">Default Value</span
                    ><input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'value')"
                      :value="targetElementData?.value"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Submit data</span
                    >
                    <div class="form-check form-switch">
                      <input
                        class="form-check-input"
                        type="checkbox"
                        role="switch"
                        id="flexSwitchCheckChecked"
                        checked
                      /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="vfb-faqs">
            <div class="vfb-faqs-item">
              <div
                @click="handleClick"
                class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
              >
                <span class="medium text-black">Decorators</span>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    fill="#94a3b8"
                    d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-close d-none"
                  aria-hidden="true"
                  focusable="false"
                  fill="#94a3b8"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div class="vfb-faqs-body bg-white" style="display: none">
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black">Prefix</span
                    ><input
                      type="text"
                      @input="setElementAttribute($event, 'prefix')"
                      :value="targetElementData?.prefix"
                      class="bg-input form-p-input-sm h-32"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">Suffix</span
                    ><input
                      type="text"
                      @input="setElementAttribute($event, 'suffix')"
                      :value="targetElementData?.suffix"
                      class="bg-input form-p-input-sm h-32"
                    />
                  </div>
                </div>
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black">Before</span
                    ><input
                      @input="setElementAttribute($event, 'before')"
                      :value="targetElementData?.before"
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">Between</span
                    ><input
                      @input="setElementAttribute($event, 'between')"
                      :value="targetElementData?.between"
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                    />
                  </div>

                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">After</span
                    ><input
                      @input="setElementAttribute($event, 'after')"
                      :value="targetElementData?.after"
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="vfb-faqs">
            <div class="vfb-faqs-item">
              <div
                @click="handleClick"
                class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
              >
                <span class="medium text-black">Layout</span>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    fill="#94a3b8"
                    d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-close d-none"
                  aria-hidden="true"
                  focusable="false"
                  fill="#94a3b8"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div class="vfb-faqs-body bg-white" style="display: none">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center vfb-faqs-body-inner border-bottom-0"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center"
                    >Size
                    <a href="##" class="vfb-learn-more ms-2" target="_blank"
                      >learn more</a
                    ></span
                  >
                  <div class="btn-group border">
                    <button
                      @click="setElementSizeAttribute($event, 'size', 'font-default')"
                      type="button"
                      class="btn fs-12 h-100 px-2"
                      :class="{
                        activeBtnClass: targetElementData?.size == 'font-default',
                      }"
                    >
                      Default</button
                    ><button
                      @click="setElementSizeAttribute($event, 'size', 'font-sm')"
                      type="button"
                      class="btn fs-12 border-start px-3"
                      :class="{
                        activeBtnClass: targetElementData?.size == 'font-sm',
                      }"
                    >
                      sm</button
                    ><button
                      @click="setElementSizeAttribute($event, 'size', 'font-md')"
                      type="button"
                      class="btn fs-12 border-start px-3"
                      :class="{
                        activeBtnClass: targetElementData?.size == 'font-md',
                      }"
                    >
                      md</button
                    ><button
                      @click="setElementSizeAttribute($event, 'size', 'font-lg')"
                      type="button"
                      class="btn fs-12 border-start px-3"
                      :class="{
                        activeBtnClass: targetElementData?.size == 'font-lg',
                      }"
                    >
                      lg
                    </button>
                  </div>
                </div>

                <section class="text-layout">
                  <div
                    class="form-text-sm d-flex flex-wrap justify-content-between align-items-center mt-2 vfb-faqs-body-inner border-bottom-0"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >
                      Columns
                      <a href="#" class="vfb-learn-more ms-2" target="_blank"
                        >learn more</a
                      >
                    </span>
                    <div class="w-100 py-2">
                      <ul
                        class="nav nav-pills border category_tabs container_tabs"
                        id="input-tab"
                        role="tablist"
                      >
                        <li class="nav-item" role="presentation">
                          <button
                            class="nav-link active text-black tabFirst w-100"
                            id="input-default-tab"
                            data-bs-toggle="pill"
                            data-bs-target="#input-default"
                            type="button"
                            role="tab"
                            aria-controls="select-default"
                            aria-selected="true"
                          >
                            Default
                          </button>
                        </li>
                        <li class="nav-item" role="presentation">
                          <button
                            class="nav-link text-black tabCenter w-100"
                            id="input-tablet-tab"
                            data-bs-toggle="pill"
                            data-bs-target="#input-tablet"
                            type="button"
                            role="tab"
                            aria-controls="select-tablet"
                            aria-selected="false"
                          >
                            Tablet
                          </button>
                        </li>
                        <li class="nav-item" role="presentation">
                          <button
                            class="nav-link text-black tablast w-100"
                            id="input-desktop-tab"
                            data-bs-toggle="pill"
                            data-bs-target="#input-desktop"
                            type="button"
                            role="tab"
                            aria-controls="select-desktop"
                            aria-selected="false"
                          >
                            Desktop
                          </button>
                        </li>
                      </ul>

                      <div class="tab-content">
                        <!-- Default Tab -->
                        <div
                          class="tab-pane fade show active"
                          id="input-default"
                          role="tabpanel"
                          aria-labelledby="input-default-tab"
                        >
                          <!-- Content for Default Tab -->
                          <section>
                            <div
                              class="w-100 d-flex justify-content-between align-items-items-center py-3"
                            >
                              <div class="fs-14 text-64748B">DEFAULT</div>
                              <div class="text-xs fs-14 text-64748B">
                                Viewport size &gt;=0px
                              </div>
                            </div>

                            <div class="w-100 py-3 tab-inner-content">
                              <ul
                                class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                                id="cont-tab"
                                role="tablist"
                              >
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link active text-black tabFirst w-100"
                                    id="input-container-tab"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-container"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-cont"
                                    aria-selected="true"
                                  >
                                    Container
                                  </button>
                                </li>
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link text-black tabCenter w-100"
                                    id="input-label-tab"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-label"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-lebal"
                                    aria-selected="false"
                                  >
                                    Label
                                  </button>
                                </li>
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link text-black tablast w-100"
                                    id="input-wrapper-tab"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-wrapper"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-Wrapper"
                                    aria-selected="false"
                                  >
                                    Wrapper
                                  </button>
                                </li>
                              </ul>

                              <div class="tab-content" id="default-tabContent">
                                <div
                                  class="tab-pane fade show active"
                                  id="input-container"
                                  role="tabpanel"
                                  aria-labelledby="input-container-tab"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">
                                          Container width:
                                        </div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.default.container ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.default.container ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.default.container ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'default',
                                              'container',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>

                                <div
                                  class="tab-pane fade"
                                  id="input-label"
                                  role="tabpanel"
                                  aria-labelledby="input-label-tab"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">Label width:</div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.default.label ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.default.label ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.default.label ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'default',
                                              'label',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>

                                <div
                                  class="tab-pane fade"
                                  id="input-wrapper"
                                  role="tabpanel"
                                  aria-labelledby="input-wrapper-tab"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">
                                          Wrapper width:
                                        </div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.default.wrapper ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.default.wrapper ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.default.wrapper ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'default',
                                              'wrapper',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </section>
                          <!-- Content for Default Tab -->
                        </div>

                        <!-- Tablet Tab -->
                        <div
                          class="tab-pane fade"
                          id="input-tablet"
                          role="tabpanel"
                          aria-labelledby="input-tablet-tab"
                        >
                          <!-- Content for Tablet Tab -->
                          <section>
                            <div
                              class="w-100 d-flex justify-content-between align-items-items-center py-3"
                            >
                              <div class="fs-14 text-64748B">TABLET</div>
                              <div class="text-xs fs-14 text-64748B">
                                Viewport size &gt;=640px
                              </div>
                            </div>

                            <div class="w-100 py-3 tab-inner-content">
                              <ul
                                class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                                id="cont-tab1"
                                role="tablist"
                              >
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link active text-black tabFirst w-100"
                                    id="input-container-tab1"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-container1"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-cont"
                                    aria-selected="true"
                                  >
                                    Container
                                  </button>
                                </li>
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link text-black tabCenter w-100"
                                    id="input-label-tab1"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-label1"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-lebal"
                                    aria-selected="false"
                                  >
                                    Label
                                  </button>
                                </li>
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link text-black tablast w-100"
                                    id="input-wrapper-tab1"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-wrapper1"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-Wrapper"
                                    aria-selected="false"
                                  >
                                    Wrapper
                                  </button>
                                </li>
                              </ul>

                              <div class="tab-content" id="default-tabContent1">
                                <div
                                  class="tab-pane fade show active"
                                  id="input-container1"
                                  role="tabpanel"
                                  aria-labelledby="input-container-tab1"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">
                                          Container width:
                                        </div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.desktop.container ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.container ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.container ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'desktop',
                                              'container',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>

                                <div
                                  class="tab-pane fade"
                                  id="input-label1"
                                  role="tabpanel"
                                  aria-labelledby="input-label-tab1"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">Label width:</div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.tablet.label ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.tablet.label ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.tablet.label ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'tablet',
                                              'label',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>

                                <div
                                  class="tab-pane fade"
                                  id="input-wrapper1"
                                  role="tabpanel"
                                  aria-labelledby="input-wrapper-tab1"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">
                                          Wrapper width:
                                        </div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.tablet.wrapper ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.tablet.wrapper ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.tablet.wrapper ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'tablet',
                                              'wrapper',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </section>
                          <!-- Content for Tablet Tab -->
                        </div>

                        <!-- Desktop Tab -->
                        <div
                          class="tab-pane fade"
                          id="input-desktop"
                          role="tabpanel"
                          aria-labelledby="input-desktop-tab"
                        >
                          <!-- Content for Desktop Tab -->
                          <section>
                            <div
                              class="w-100 d-flex justify-content-between align-items-items-center py-3"
                            >
                              <div class="fs-14 text-64748B">DESKTOP</div>
                              <div class="text-xs fs-14 text-64748B">
                                Viewport size &gt;=1024px
                              </div>
                            </div>

                            <div class="w-100 py-3 tab-inner-content">
                              <ul
                                class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                                id="cont-tab2"
                                role="tablist"
                              >
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link active text-black tabFirst w-100"
                                    id="input-container-tab2"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-container2"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-cont"
                                    aria-selected="true"
                                  >
                                    Container
                                  </button>
                                </li>
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link text-black tabCenter w-100"
                                    id="input-label-tab2"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-label2"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-lebal"
                                    aria-selected="false"
                                  >
                                    Label
                                  </button>
                                </li>
                                <li class="nav-item" role="presentation">
                                  <button
                                    class="nav-link text-black tablast w-100"
                                    id="input-wrapper-tab2"
                                    data-bs-toggle="pill"
                                    data-bs-target="#input-wrapper2"
                                    type="button"
                                    role="tab"
                                    aria-controls="pills-Wrapper"
                                    aria-selected="false"
                                  >
                                    Wrapper
                                  </button>
                                </li>
                              </ul>

                              <div class="tab-content" id="default-tabContent2">
                                <div
                                  class="tab-pane fade show active"
                                  id="input-container2"
                                  role="tabpanel"
                                  aria-labelledby="input-container-tab2"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">
                                          Container width:
                                        </div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.desktop.container ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.container ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.container ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'desktop',
                                              'container',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>

                                <div
                                  class="tab-pane fade"
                                  id="input-label2"
                                  role="tabpanel"
                                  aria-labelledby="input-label-tab2"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">Label width:</div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.desktop.label ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.label ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.label ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'desktop',
                                              'label',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>

                                <div
                                  class="tab-pane fade"
                                  id="input-wrapper2"
                                  role="tabpanel"
                                  aria-labelledby="input-wrapper-tab2"
                                >
                                  <div class="w-100">
                                    <div class="mt-3">
                                      <div
                                        class="w-100 d-flex justify-content-between align-items-items-center"
                                      >
                                        <div class="fs-14 text-64748B">
                                          Wrapper width:
                                        </div>
                                        <div class="text-xs fs-14 text-64748B">1/12</div>
                                      </div>
                                      <div class="btn-group border w-100 mt-3">
                                        <button
                                          v-for="column in 12"
                                          :key="column"
                                          type="button"
                                          class="btn fs-12 bg-light h-100 px-1"
                                          :class="{
                                            activeBtnClass:
                                              targetElementColumns.desktop.wrapper ===
                                              `col-lg-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.wrapper ===
                                              `col-md-${column}`,
                                            activeBtnClass:
                                              targetElementColumns.desktop.wrapper ===
                                              `col-sm-${column}`,
                                          }"
                                          @click="
                                            setElementColumns(
                                              $event,
                                              'desktop',
                                              'wrapper',
                                              column
                                            )
                                          "
                                        >
                                          {{ column }}
                                        </button>
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </section>
                          <!-- Content for Desktop Tab -->
                        </div>
                      </div>
                    </div>
                  </div>
                </section>
              </div>
            </div>
          </div>
          <div class="vfb-faqs">
            <div class="vfb-faqs-item">
              <div
                @click="handleClick"
                class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
              >
                <span class="medium text-black">Validation</span>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    fill="#94a3b8"
                    d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-close d-none"
                  aria-hidden="true"
                  focusable="false"
                  fill="#94a3b8"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div class="vfb-faqs-body bg-white" style="display: none">
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Input Field</span
                    ><input
                      type="text"
                      placeholder="Default"
                      class="bg-input form-p-input-sm h-32"
                    />
                  </div>
                </div>
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Required</span
                    >
                    <div class="form-check form-switch">
                      <input
                        class="form-check-input"
                        type="checkbox"
                        role="switch"
                        @change="setCheckboxElementAttribute($event, 'isRequired')"
                      /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                    </div>
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Nullable</span
                    >
                    <div class="form-check form-switch">
                      <input
                        class="form-check-input"
                        type="checkbox"
                        role="switch"
                        @change="setCheckboxElementAttribute($event, 'isNullable')"
                      /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                    </div>
                  </div>
                </div>
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center"
                      >Unique
                      <a href="##" class="vfb-learn-more ms-2" target="_blank"
                        >learn more</a
                      ></span
                    >
                    <div class="form-check form-switch">
                      <input
                        class="form-check-input"
                        type="checkbox"
                        role="switch"
                        @change="setCheckboxElementAttribute($event, 'isUnique')"
                      /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                    </div>
                  </div>
                </div>

                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black">Min length</span
                    ><input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'minlength')"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">Max length</span>
                    <input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'maxlength')"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">Exact length</span
                    ><input type="text" class="bg-input form-p-input-sm h-32" />
                  </div>
                </div>

                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black">Regex</span
                    ><input
                      type="text"
                      placeholder="eg. /^.+$/i"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'pattern')"
                    />
                  </div>
                </div>

                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black position-relative align-items-center"
                      >Additional rules
                      <a href="##" class="vfb-learn-more ms-2" target="_blank"
                        >learn more</a
                      ></span
                    >
                    <button class="inline-block border-0 form-bg-primary form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm" @click="addItem">+Add </button>
                  </div>
                </div>
                <div>
                  <div
                    v-for="(item, index) in items"
                    :key="index"
                    class="add_inner vfb-faqs-item-inner"
                  >
                    <button
                      @click="removeItem(index, 'rules')"
                      :data="targetElementData?.rules"
                    >
                      X
                    </button>
                    <select
                      class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                      v-model="item.type"
                      :data="targetElementData?.rules"
                      @change="handleTypeChange(index, 'rules')"
                    >
                      <option disabled selected>Choose rule</option>
                      <option value="array">Array</option>
                      <option value="gt">Greater than</option>
                      <option value="gte">Greater than or equal</option>
                      <option value="lt">Less than</option>
                      <option value="lte">Less than or equal</option>
                    </select>
                    <select
                      class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                      v-if="item.type !== 'array'"
                      v-model="item.field"
                      @change="handleFieldChange(index, 'rules')"
                      :data="targetElementData?.rules"
                    >
                      <option disabled selected>Other field</option>
                      <option v-for="(element, index) in getListOfElements" :key="index">
                        {{ element.identification }}
                      </option>
                    </select>
                  </div>
                  

                  <div class="vfb-faqs-body-inner border-0">
                    <div
                      v-for="(item, index) in items_AO"
                      :key="index"
                      class="add_inner position-relative"
                    >
                      <button
                        @click="removeItem(index, 'rules')"
                        :data="targetElementData?.rules"
                        class="close-svg-add-more-option border-0 p-0"
                      >
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 320 512"
                          fill="currentColor"
                        >
                          <path
                            data-v-c98426aa=""
                            d="M193.94 256L296.5 153.44l21.15-21.15c3.12-3.12 3.12-8.19 0-11.31l-22.63-22.63c-3.12-3.12-8.19-3.12-11.31 0L160 222.06 36.29 98.34c-3.12-3.12-8.19-3.12-11.31 0L2.34 120.97c-3.12 3.12-3.12 8.19 0 11.31L126.06 256 2.34 379.71c-3.12 3.12-3.12 8.19 0 11.31l22.63 22.63c3.12 3.12 8.19 3.12 11.31 0L160 289.94 262.56 392.5l21.15 21.15c3.12 3.12 8.19 3.12 11.31 0l22.63-22.63c3.12-3.12 3.12-8.19 0-11.31L193.94 256z"
                          ></path>
                        </svg>
                      </button>
                      <strong class="text-64748B mt-2 mb-1">AND</strong>
                      <select
                        class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                        v-model="item.type"
                        @change="handleTypeChange(index, 'rules')"
                        :data="targetElementData?.rules"
                      >
                        <option value="" selected disabled>Choose rule</option>
                        <option value="array">Array</option>
                        <option value="gt">Greater than</option>
                        <option value="gte">Greater than or equal</option>
                        <option value="lt">Less than</option>
                        <option value="lte">Less than or equal</option>
                      </select>
                      <select
                        v-if="item.type !== 'array'"
                        class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                        v-model="item.field"
                        @change="handleFieldChange(index, 'rules')"
                        :data="targetElementData?.rules"
                      >
                        <option value="" disabled>Other field</option>
                        <option
                          v-for="(element, index) in getListOfElements"
                          :key="index"
                        >
                          {{ element.identification }}
                        </option>
                      </select>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="vfb-faqs">
            <div class="vfb-faqs-item">
              <div
                @click="handleClick"
                class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
              >
                <span class="medium text-black">Conditions</span>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    fill="#94a3b8"
                    d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-close d-none"
                  aria-hidden="true"
                  focusable="false"
                  fill="#94a3b8"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div class="vfb-faqs-body bg-white" style="display: none">
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span class="fs-14 text-black">The element has no conditions</span>
                    <div
                      @click="showModel($event)"
                      class="inline-block form-bg-primary form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                      id="validation.validation_wrapper.rules-add-button"
                      role="button"
                      tabindex="0"
                    >
                      + Edit
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="vfb-faqs">
            <div class="vfb-faqs-item">
              <div
                @click="handleClick"
                class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
              >
                <span class="medium text-black">Attributes</span>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    fill="#94a3b8"
                    d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
                <svg
                  width="12px"
                  height="12px"
                  class="vfb-icon vfb-config-form-header-collapse-close d-none"
                  aria-hidden="true"
                  focusable="false"
                  fill="#94a3b8"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 384 512"
                >
                  <path
                    class=""
                    d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div class="vfb-faqs-body bg-white" style="display: none">
                <div class="vfb-faqs-body-inner">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Disabled</span
                    >
                    <div class="form-check form-switch">
                      <input
                        class="form-check-input"
                        type="checkbox"
                        role="switch"
                        @change="setCheckboxElementAttribute($event, 'disabled')"
                      /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                    </div>
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                      >Readonly</span
                    >
                    <div class="form-check form-switch">
                      <input
                        class="form-check-input"
                        type="checkbox"
                        role="switch"
                        @change="setCheckboxElementAttribute($event, 'readonly')"
                      /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                    </div>
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">ID</span
                    ><input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'id')"
                      :value="targetElementData?.id"
                    />
                  </div>
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  >
                    <span class="fs-14 text-black">Autocompelete</span
                    ><input
                      type="text"
                      class="bg-input form-p-input-sm h-32"
                      @input="setElementAttribute($event, 'autocomplete')"
                      :value="targetElementData?.autocomplete"
                    />
                  </div>
                </div>
                <div class="vfb-faqs-body-inner bg-light">
                  <div
                    class="form-text-sm d-flex justify-content-between align-items-center"
                  >
                    <span
                      class="fs-14 text-black position-relative d-flex align-items-center"
                    >
                      Custom attributes
                      <a href="#" class="vfb-learn-more ms-2" target="_blank"
                        >learn more</a
                      >
                    </span>
                    <button
                      @click="addAttributes"
                      class="inline-block form-bg-primary border-0 form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                      role="button"
                      tabindex="0"
                    >
                      + Add
                    </button>
                  </div>
                  <div aria-labelledby="attributes.attrs__label">
                    <div
                      v-for="(attribute, key) in targetElementCustomAttributesArr"
                      :key="attribute.name"
                      class="d-flex align-items-center border-bottom checkclosehover position-relative mt-3"
                    >
                      <button
                        @click="removeElementCustomAttribute($event, key)"
                        class="close-svg-add-more-option border-0 p-0"
                      >
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 320 512"
                          fill="currentColor"
                        >
                          <path
                            d="M193.94 256L296.5 153.44l21.15-21.15c3.12-3.12 3.12-8.19 0-11.31l-22.63-22.63c-3.12-3.12-8.19-3.12-11.31 0L160 222.06 36.29 98.34c-3.12-3.12-8.19-3.12-11.31 0L2.34 120.97c-3.12 3.12-3.12 8.19 0 11.31L126.06 256 2.34 379.71c-3.12 3.12-3.12 8.19 0 11.31l22.63 22.63c3.12 3.12 8.19 3.12 11.31 0L160 289.94 262.56 392.5l21.15 21.15c3.12 3.12 8.19 3.12 11.31 0l22.63-22.63c3.12-3.12 3.12-8.19 0-11.31L193.94 256z"
                          />
                        </svg>
                      </button>
                      <input
                        type="text"
                        placeholder="Name"
                        :v-model="attribute.name"
                        class="add-more-option border-0 bg-transparent h-32 w-100 px-2 py-1 labelInput"
                      />
                      <span class="px-2">
                        <svg
                          class="vfb-icon cursor-pointer"
                          aria-hidden="true"
                          focusable="false"
                          role="img"
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <path
                            class=""
                            fill="currentColor"
                            d="M311.03 131.515l-7.071 7.07c-4.686 4.686-4.686 12.284 0 16.971L387.887 239H12c-6.627 0-12 5.373-12 12v10c0 6.627 5.373 12 12 12h375.887l-83.928 83.444c-4.686 4.686-4.686 12.284 0 16.971l7.071 7.07c4.686 4.686 12.284 4.686 16.97 0l116.485-116c4.686-4.686 4.686-12.284 0-16.971L328 131.515c-4.686-4.687-12.284-4.687-16.97 0z"
                          />
                        </svg>
                      </span>
                      <input
                        @input="makeElementCustomAttribute($event)"
                        type="text"
                        placeholder="Value"
                        :v-model="attribute.value"
                        class="add-more-option border-0 bg-transparent px-2 py-1 h-32 w-100 valueInput"
                      />
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <br />
        <br />
        <br />
        <br />
        <br />
      </div>
    </div>
  </section>
  <!-- <  ------------------------------ > -->

  <!-- < MULTISELECT  ------------------------------ > MULTISELECT -->
  <div class="vfb-right-container" style="right: -500px" id="multiSelectrightMenu">
    <div class="position-relative h-100">
      <div class="vfb-panels-wrapper-multiselect">
        <div class="vfb-config-panel-header-container">
          <div class="vfb-config-panel-header">
            <div class="vfb-config-panel-header-wrapper-left">
              <span
                class="vfb-config-panel-header-close"
                tabindex="0"
                @click="multiselectClose"
                role="button"
                aria-label="Close config panel"
                ><svg
                  class="vfb-icon vfb-config-panel-header-close-icon"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 320 512"
                >
                  <path
                    class=""
                    fill="currentColor"
                    d="M207.6 256l107.72-107.72c6.23-6.23 6.23-16.34 0-22.58l-25.03-25.03c-6.23-6.23-16.34-6.23-22.58 0L160 208.4 52.28 100.68c-6.23-6.23-16.34-6.23-22.58 0L4.68 125.7c-6.23 6.23-6.23 16.34 0 22.58L112.4 256 4.68 363.72c-6.23 6.23-6.23 16.34 0 22.58l25.03 25.03c6.23 6.23 16.34 6.23 22.58 0L160 303.6l107.72 107.72c6.23 6.23 16.34 6.23 22.58 0l25.03-25.03c6.23-6.23 6.23-16.34 0-22.58L207.6 256z"
                  ></path>
                  <!--v-if-->
                </svg></span
              ><span class="vfb-config-panel-header-label">{{
                targetElementData?.identification
              }}</span>
            </div>
            <div class="vfb-config-panel-header-wrapper-right">
              <!-- Clone -->
              <div
                @click="cloneSelectElement($event)"
                class="vfb-config-panel-header-clone"
                tabindex="0"
                role="button"
                aria-label="Clone"
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
                    d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zm-80 464c0 8.82-7.18 16-16 16H48c-8.82 0-16-7.18-16-16V144c0-8.82 7.18-16 16-16h48v240c0 26.51 21.49 48 48 48h240v48zm96-96c0 8.82-7.18 16-16 16H144c-8.82 0-16-7.18-16-16V48c0-8.82 7.18-16 16-16h320c8.82 0 16 7.18 16 16v320z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <!-- Remove -->
              <div
                class="vfb-config-panel-header-remove"
                tabindex="0"
                role="button"
                aria-label="Remove"
                @click="deleteSelectElement($event)"
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
                    d="M296 432h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zm-160 0h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zM440 64H336l-33.6-44.8A48 48 0 0 0 264 0h-80a48 48 0 0 0-38.4 19.2L112 64H8a8 8 0 0 0-8 8v16a8 8 0 0 0 8 8h24v368a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V96h24a8 8 0 0 0 8-8V72a8 8 0 0 0-8-8zM171.2 38.4A16.1 16.1 0 0 1 184 32h80a16.1 16.1 0 0 1 12.8 6.4L296 64H152zM384 464a16 16 0 0 1-16 16H80a16 16 0 0 1-16-16V96h320zm-168-32h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div
                class="vfb-config-panel-header-collapse vv-vfb-icon-plus"
                tabindex="0"
                role="button"
                aria-label="Expand all"
                @click="ColapsToggleExpand"
              >
                <svg
                  class="vfb-icon vfb-config-panel-header-collapse-icon-open"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 448 512"
                >
                  <path
                    class=""
                    fill="currentColor"
                    d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 206h-98v-98c0-6.6-5.4-12-12-12h-12c-6.6 0-12 5.4-12 12v98h-98c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h98v98c0 6.6 5.4 12 12 12h12c6.6 0 12-5.4 12-12v-98h98c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
              <div
                class="vfb-config-panel-header-collapse d-none vv-vfb-icon-close"
                tabindex="0"
                role="button"
                aria-label="Collapse all"
                @click="ColapsToggleClose"
              >
                <svg
                  class="vfb-icon vfb-config-panel-header-collapse-icon-close"
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 448 512"
                >
                  <path
                    class=""
                    fill="currentColor"
                    d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 242c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12H108c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h232z"
                  ></path>
                  <!--v-if-->
                </svg>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Properties</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center"
                >
                  <span class="fs-14 text-black">Name</span
                  ><input
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                    @input="setMuiltiSelect($event, 'name')"
                    :value="targetElementData?.name"
                  />
                </div>
              </div>
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span class="fs-14 text-black">Label</span
                  ><input
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                    @input="setMuiltiSelect($event, 'label')"
                    :value="targetElementData?.label"
                  />
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Tooltip</span
                  >
                  <input
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                    @input="setMuiltiSelect($event, 'title')"
                    :value="targetElementData?.title"
                  />
                </div>
              </div>
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Placeholder</span
                  >
                  <input
                    type="text"
                    class="bg-input w-50 form-p-input-sm h-32"
                    @input="setMuiltiSelect($event, 'placeholder')"
                    :value="targetElementData?.placeholder"
                  />
                </div>
                <!-- <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative form-bg-info d-flex align-items-center"
                    >Preview width</span
                  >
                  <div class="btn-group border w-50">
                    <button
                      type="button"
                      class="btn fs-12 vf-primary text-white h-100 px-2"
                    >
                      Default</button
                    ><button type="button" class="btn fs-12 border-start px-3">
                      Off
                    </button>
                  </div>
                </div> -->
              </div>
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center"
                    >Description</span
                  >
                  <input
                    type="text"
                    class="bg-input w-50 form-p-input-sm h-32"
                    :value="targetElementData?.description"
                    @input="setMuiltiSelect($event, 'description')"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Multiselect options</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Native</span
                  >
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      checked
                      @change="setMuiltiSelect($event, 'isNative')"
                      :value="targetElementData?.isNative"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
              </div>
              <div class="vfb-faqs-body-inner">
                <div class="fs-14 text-64748B medium">SEARCH</div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-3"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center"
                    >Search</span
                  >
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      checked
                      @change="setMuiltiSelect($event, 'isSearch')"
                      :value="targetElementData?.isSearch"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Strict search</span
                  >
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      checked
                      @change="setMuiltiSelect($event, 'isStrictSearch')"
                      :value="targetElementData?.isStrictSearch"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Track by key</span
                  >
                  <div class="w-50">
                    <input
                      type="text"
                      placeholder="label"
                      class="bg-input w-100 form-p-input-sm h-32"
                      :value="targetElementData?.trackByKey"
                      @input="setMuiltiSelect($event, 'trackByKey')"
                    />
                  </div>
                </div>
              </div>

              <div class="vfb-faqs-body-inner">
                <div class="fs-14 text-64748B medium">BEHAVIOR</div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-3"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Can deselect
                  </span>
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      @change="setMuiltiSelect($event, 'deselect')"
                      :value="targetElementData?.deselect"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Can clear
                  </span>
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      @change="setMuiltiSelect($event, 'isClear')"
                      :value="targetElementData?.isClear"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Close on select
                  </span>
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      @change="setMuiltiSelect($event, 'closeOnSelect')"
                      :value="targetElementData?.closeOnSelect"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Hide selected
                  </span>
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      @change="setMuiltiSelect($event, 'hideSelected')"
                      :value="targetElementData?.hideSelected"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
              </div>
              <div class="vfb-faqs-body-inner">
                <div class="fs-14 text-64748B medium">UI</div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-3"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center"
                    >Display caret
                  </span>
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      checked
                      id="flexSwitchCheckChecked"
                      @change="setMuiltiSelect($event, 'displayCaret')"
                      :value="targetElementData?.displayCaret"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Truncate
                  </span>
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      @change="setMuiltiSelect($event, 'truncate')"
                      :value="targetElementData?.truncate"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-none justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center"
                    >Open direction
                  </span>
                  <div class="btn-group border">
                    <button type="button" class="btn fs-12 h-100 px-3">top</button>
                    <button
                      type="button"
                      class="btn text-white vf-primary fs-12 border-start px-2"
                    >
                      button
                    </button>
                  </div>
                </div>
                <div
                  class="form-text-sm d-none justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Option limit</span
                  >
                  <input
                    type="number"
                    placeholder="no limit"
                    class="bg-input w-50 form-p-input-sm h-32"
                  />
                </div>
              </div>
              <div class="vfb-faqs-body-inner d-none">
                <div
                  class="form-text-sm d-none justify-content-between align-items-center"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Max options
                  </span>
                  <input
                    type="number"
                    placeholder="no limit"
                    class="bg-input w-50 form-p-input-sm h-32"
                  />
                </div>
              </div>
              <div class="vfb-faqs-body-inner d-none">
                <div
                  class="form-text-sm d-none justify-content-between align-items-center"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Options label (x=1)
                  </span>
                  <input
                    type="text"
                    placeholder="default"
                    class="bg-input w-50 form-p-input-sm h-32"
                  />
                </div>
                <div
                  class="form-text-sm d-none justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >No options text
                  </span>
                  <input
                    type="text"
                    placeholder="default"
                    class="bg-input w-50 form-p-input-sm h-32"
                  />
                </div>
                <div
                  class="form-text-sm d-none justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >No results text
                  </span>
                  <input
                    type="text"
                    placeholder="default"
                    class="bg-input w-50 form-p-input-sm h-32"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Data</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div
                class="form-text-sm d-flex flex-wrap justify-content-between align-items-center mt-2 vfb-faqs-body-inner border-bottom-0"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                >
                  DATA SOURCE
                  <a href="#" class="vfb-learn-more ms-2" target="_blank">learn more</a>
                </span>
                <div class="w-100 py-2">
                  <ul
                    class="nav nav-pills border category_tabs container_tabs"
                    id="multiimage-tab"
                    role="tablist"
                  >
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link active text-black tabFirst w-100"
                        id="multiimage-default-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#multiimage-default"
                        type="button"
                        role="tab"
                        aria-controls="multiimage-default"
                        aria-selected="true"
                        @click="selectDataSource('list')"
                      >
                        List
                      </button>
                    </li>
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link text-black tabCenter w-100"
                        id="multiimage-tablet-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#multiimage-tablet"
                        type="button"
                        role="tab"
                        aria-controls="multiimage-tablet"
                        aria-selected="false"
                        @click="selectDataSource('json')"
                      >
                        JSON
                      </button>
                    </li>
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link text-black tablast w-100"
                        id="multiimage-desktop-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#multiimage-desktop"
                        type="button"
                        role="tab"
                        aria-controls="multiimage-desktop"
                        aria-selected="false"
                        @click="selectDataSource('endpoint')"
                      >
                        End Point
                      </button>
                    </li>
                  </ul>

                  <div class="tab-content">
                    <!-- First Tab Content -->
                    <div
                      class="tab-pane fade show active"
                      id="multiimage-default"
                      role="tabpanel"
                      aria-labelledby="multiimage-default-tab"
                    >
                      <div class="vfb-faqs-body-inner">
                        <div class="fs-14 text-64748B medium">CREATE OPTION</div>
                        <div
                          v-for="(attribute, key) in targetElementData.options"
                          :key="attribute.name"
                          class="d-flex align-items-center border-bottom checkclosehover position-relative mt-3"
                        >
                          <button
                            @click="removeSelectOption($event, key)"
                            class="close-svg-add-more-option border-0 p-0"
                          >
                          <svg
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 320 512"
                      fill="currentColor"
                    >
                      <path
                        d="M193.94 256L296.5 153.44l21.15-21.15c3.12-3.12 3.12-8.19 0-11.31l-22.63-22.63c-3.12-3.12-8.19-3.12-11.31 0L160 222.06 36.29 98.34c-3.12-3.12-8.19-3.12-11.31 0L2.34 120.97c-3.12 3.12-3.12 8.19 0 11.31L126.06 256 2.34 379.71c-3.12 3.12-3.12 8.19 0 11.31l22.63 22.63c3.12 3.12 8.19 3.12 11.31 0L160 289.94 262.56 392.5l21.15 21.15c3.12 3.12 8.19 3.12 11.31 0l22.63-22.63c3.12-3.12 3.12-8.19 0-11.31L193.94 256z"
                      />
                    </svg>
                          </button>
                          <input
                            type="text"
                            placeholder="Name"
                            :value="attribute.name"
                            :v-model="attribute.name"
                            class="add-more-option border-0 bg-transparent h-32 w-100 px-2 py-1 labelInput"
                          />
                          <svg
                      class="vfb-icon cursor-pointer"
                      aria-hidden="true"
                      focusable="false"
                      role="img"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 448 512"
                    >
                      <path
                        class=""
                        fill="currentColor"
                        d="M311.03 131.515l-7.071 7.07c-4.686 4.686-4.686 12.284 0 16.971L387.887 239H12c-6.627 0-12 5.373-12 12v10c0 6.627 5.373 12 12 12h375.887l-83.928 83.444c-4.686 4.686-4.686 12.284 0 16.971l7.071 7.07c4.686 4.686 12.284 4.686 16.97 0l116.485-116c4.686-4.686 4.686-12.284 0-16.971L328 131.515c-4.686-4.687-12.284-4.687-16.97 0z"
                      />
                    </svg>
                          <input
                            @input="makeSelectElemenOptions($event)"
                            type="text"
                            placeholder="Value"
                            :value="attribute.value"
                            :v-model="attribute.value"
                            class="add-more-option border-0 bg-transparent px-2 py-1 h-32 w-100 valueInput"
                          />
                        </div>
                        <div class="mt-3">
                          <button
                            class="btn vf-primary text-white btn-sm rounded-2 text-sm fs-14"
                            @click="addOption()"
                          >
                            Add option
                          </button>
                        </div>
                      </div>
                    </div>

                    <!-- Second Tab Content (Empty) -->
                    <div
                      class="tab-pane fade"
                      id="multiimage-tablet"
                      role="tabpanel"
                      aria-labelledby="multiimage-tablet-tab"
                    >
                      <!-- Content for Tablet Tab (Empty) -->
                      <textarea
                        @input="setOptionsAsJson($event)"
                        name="json"
                        id="data.items_wrapper.json"
                        class="w-full mt-3 form-p-input-sm w-100 bg-input h-full form-p-input-sm form-radius-large-sm form-text-sm with-floating:form-p-input-floating-sm form-color-input group-hover:form-color-input-hover form-autofill-default"
                        placeholder='Copy your JSON here, eg:
[
  { "value": "vuejs", "label": "Vue.js" },
  { "value": "react", "label": "React" }
]'
                        rows="5"
                        aria-labelledby="data.items_wrapper.json__label"
                        aria-describedby="data.items_wrapper.json__description data.items_wrapper.json__info"
                        aria-invalid="false"
                        aria-errormessage="data.items_wrapper.json__error"
                        aria-disabled="false"
                        aria-busy="false"
                        >{{ targetElementData?.json }}</textarea
                      >
                    </div>

                    <!-- Third Tab Content (Empty) -->
                    <div
                      class="tab-pane fade"
                      id="multiimage-desktop"
                      role="tabpanel"
                      aria-labelledby="multiimage-desktop-tab"
                    >
                      <!-- Content for Desktop Tab (Empty) -->
                      <textarea
                        name="json"
                        id="data.items_wrapper.json"
                        class="w-full mt-3 form-p-input-sm w-100 bg-input h-full form-p-input-sm form-radius-large-sm form-text-sm with-floating:form-p-input-floating-sm form-color-input group-hover:form-color-input-hover form-autofill-default"
                        placeholder="https://x.com/{elementPath|'default'}/list"
                        rows="5"
                        aria-labelledby="data.items_wrapper.json__label"
                        aria-describedby="data.items_wrapper.json__description data.items_wrapper.json__info"
                        aria-invalid="false"
                        aria-errormessage="data.items_wrapper.json__error"
                        aria-disabled="false"
                        aria-busy="false"
                        @input="setDataSourceUrl($event)"
                        >{{ targetElementData?.endpoint }}</textarea
                      >
                    </div>
                  </div>
                </div>
              </div>

              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-none justify-content-between align-items-center"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center"
                    >Default</span
                  >
                  <div
                    class="vfb_form_fonts vfb_general_form d-flex justify-content-end position-relative"
                  >
                    <div class="position-relative">
                      <div class="selected-tags mt-0 form-control">
                        <span
                          v-for="selectedItem in uniqueSelectedItems"
                          :key="selectedItem.id"
                          @click="removeSelectedItem(selectedItem, 'default_values')"
                          :data="targetElementData?.default_values"
                        >
                          {{ selectedItem.name }}
                          <span class="remove-tag">x</span>
                        </span>
                        <input
                          v-model="searchTerm"
                          @click="toggleDefaultUl($event)"
                          readonly
                          class="w-100 border-0 bg-transparent"
                          placeholder="Select..."
                        />
                      </div>
                      <ul v-show="showDefaultUl" class="default_value_ul">
                        <li
                          v-for="item in options"
                          :value="index"
                          :key="item.id"
                          @click="selectItem(item, 'default_values')"
                          :data="targetElementData?.default_values"
                        >
                          {{ item.name }}
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Use object value

                    <a href="##" class="vfb-learn-more ms-2" target="_blank"
                      >learn more</a
                    ></span
                  >
                  <div class="form-check form-switch">
                    <input
                      @change="setMuiltiSelect($event, 'object_value')"
                      :value="targetElementData?.object_value"
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                      checked
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center"
                    >Submit data</span
                  >
                  <div class="form-check form-switch">
                    <input
                      @change="setMuiltiSelect($event, 'submit_data')"
                      :value="targetElementData?.submit_data"
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Decorators</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center"
                >
                  <span class="fs-14 text-black">Before</span>
                  <input
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                    @input="setMuiltiSelect($event, 'before')"
                    :value="targetElementData?.before"
                  />
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span class="fs-14 text-black">Between </span
                  ><input
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                    @input="setMuiltiSelect($event, 'between')"
                    :value="targetElementData?.between"
                  />
                </div>

                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span class="fs-14 text-black">After</span>
                  <input
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                    @input="setMuiltiSelect($event, 'after')"
                    :value="targetElementData?.after"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Layout</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div
                class="form-text-sm d-flex justify-content-between align-items-center vfb-faqs-body-inner border-bottom-0"
              >
                <span class="fs-14 text-black position-relative d-flex align-items-center"
                  >Size
                  <a href="##" class="vfb-learn-more ms-2" target="_blank"
                    >learn more</a
                  ></span
                >
                <div class="btn-group border">
                  <button
                    @click="setElementSizeAttribute($event, 'size', 'font-default')"
                    type="button"
                    class="btn fs-12 h-100 px-2"
                    :class="{
                      activeBtnClass: targetElementData?.size == 'font-default',
                    }"
                  >
                    Default</button
                  ><button
                    @click="setElementSizeAttribute($event, 'size', 'font-sm')"
                    type="button"
                    class="btn fs-12 border-start px-3"
                    :class="{
                      activeBtnClass: targetElementData?.size == 'font-sm',
                    }"
                  >
                    sm</button
                  ><button
                    @click="setElementSizeAttribute($event, 'size', 'font-md')"
                    type="button"
                    class="btn fs-12 border-start px-3"
                    :class="{
                      activeBtnClass: targetElementData?.size == 'font-md',
                    }"
                  >
                    md</button
                  ><button
                    @click="setElementSizeAttribute($event, 'size', 'font-lg')"
                    type="button"
                    class="btn fs-12 border-start px-3"
                    :class="{
                      activeBtnClass: targetElementData?.size == 'font-lg',
                    }"
                  >
                    lg
                  </button>
                </div>
              </div>

              <section class="multiselect-layout">
                <div
                  class="form-text-sm d-flex flex-wrap justify-content-between align-items-center mt-2 vfb-faqs-body-inner border-bottom-0"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >
                    Columns
                    <a href="#" class="vfb-learn-more ms-2" target="_blank">learn more</a>
                  </span>
                  <div class="w-100 py-2">
                    <ul
                      class="nav nav-pills border category_tabs container_tabs"
                      id="multiselect-tab"
                      role="tablist"
                    >
                      <li class="nav-item" role="presentation">
                        <button
                          class="nav-link active text-black tabFirst w-100"
                          id="multiselect-default-tab"
                          data-bs-toggle="pill"
                          data-bs-target="#multiselect-default"
                          type="button"
                          role="tab"
                          aria-controls="select-default"
                          aria-selected="true"
                        >
                          Default
                        </button>
                      </li>
                      <li class="nav-item" role="presentation">
                        <button
                          class="nav-link text-black tabCenter w-100"
                          id="multiselect-tablet-tab"
                          data-bs-toggle="pill"
                          data-bs-target="#multiselect-tablet"
                          type="button"
                          role="tab"
                          aria-controls="select-tablet"
                          aria-selected="false"
                        >
                          Tablet
                        </button>
                      </li>
                      <li class="nav-item" role="presentation">
                        <button
                          class="nav-link text-black tablast w-100"
                          id="multiselect-desktop-tab"
                          data-bs-toggle="pill"
                          data-bs-target="#multiselect-desktop"
                          type="button"
                          role="tab"
                          aria-controls="select-desktop"
                          aria-selected="false"
                        >
                          Desktop
                        </button>
                      </li>
                    </ul>

                    <div class="tab-content">
                      <!-- Default Tab -->
                      <div
                        class="tab-pane fade show active"
                        id="multiselect-default"
                        role="tabpanel"
                        aria-labelledby="multiimage-default-tab"
                      >
                        <!-- Content for Default Tab -->
                        <section>
                          <div
                            class="w-100 d-flex justify-content-between align-items-items-center py-3"
                          >
                            <div class="fs-14 text-64748B">DEFAULT</div>
                            <div class="text-xs fs-14 text-64748B">
                              Viewport size &gt;=0px
                            </div>
                          </div>

                          <div class="w-100 py-3 tab-inner-content">
                            <ul
                              class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                              id="cont-tab"
                              role="tablist"
                            >
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link active text-black tabFirst w-100"
                                  id="multiselect-container-tab"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-container"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-cont"
                                  aria-selected="true"
                                >
                                  Container
                                </button>
                              </li>
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link text-black tabCenter w-100"
                                  id="multiselect-label-tab"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-label"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-lebal"
                                  aria-selected="false"
                                >
                                  Label
                                </button>
                              </li>
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link text-black tablast w-100"
                                  id="multiselect-wrapper-tab"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-wrapper"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-Wrapper"
                                  aria-selected="false"
                                >
                                  Wrapper
                                </button>
                              </li>
                            </ul>

                            <div class="tab-content" id="default-tabContent">
                              <div
                                class="tab-pane fade show active"
                                id="multiselect-container"
                                role="tabpanel"
                                aria-labelledby="multiimage-container-tab"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">
                                        Container width:
                                      </div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.default.container ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.default.container ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.default.container ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'default',
                                            'container',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>

                              <div
                                class="tab-pane fade"
                                id="multiselect-label"
                                role="tabpanel"
                                aria-labelledby="multiimage-label-tab"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">Label width:</div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.default.label ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.default.label ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.default.label ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'default',
                                            'label',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>

                              <div
                                class="tab-pane fade"
                                id="multiselect-wrapper"
                                role="tabpanel"
                                aria-labelledby="multiimage-wrapper-tab"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">Wrapper width:</div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.default.wrapper ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.default.wrapper ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.default.wrapper ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'default',
                                            'wrapper',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </section>
                        <!-- Content for Default Tab -->
                      </div>

                      <!-- Tablet Tab -->
                      <div
                        class="tab-pane fade"
                        id="multiselect-tablet"
                        role="tabpanel"
                        aria-labelledby="multiimage-tablet-tab"
                      >
                        <!-- Content for Tablet Tab -->
                        <section>
                          <div
                            class="w-100 d-flex justify-content-between align-items-items-center py-3"
                          >
                            <div class="fs-14 text-64748B">TABLET</div>
                            <div class="text-xs fs-14 text-64748B">
                              Viewport size &gt;=640px
                            </div>
                          </div>

                          <div class="w-100 py-3 tab-inner-content">
                            <ul
                              class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                              id="cont-tab1"
                              role="tablist"
                            >
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link active text-black tabFirst w-100"
                                  id="multiselect-container-tab1"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-container1"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-cont"
                                  aria-selected="true"
                                >
                                  Container
                                </button>
                              </li>
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link text-black tabCenter w-100"
                                  id="multiselect-label-tab1"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-label1"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-lebal"
                                  aria-selected="false"
                                >
                                  Label
                                </button>
                              </li>
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link text-black tablast w-100"
                                  id="multiselect-wrapper-tab1"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-wrapper1"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-Wrapper"
                                  aria-selected="false"
                                >
                                  Wrapper
                                </button>
                              </li>
                            </ul>

                            <div class="tab-content" id="default-tabContent1">
                              <div
                                class="tab-pane fade show active"
                                id="multiselect-container1"
                                role="tabpanel"
                                aria-labelledby="multiimage-container-tab1"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">
                                        Container width:
                                      </div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.desktop.container ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.container ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.container ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'desktop',
                                            'container',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>

                              <div
                                class="tab-pane fade"
                                id="multiselect-label1"
                                role="tabpanel"
                                aria-labelledby="multiimage-label-tab1"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">Label width:</div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.tablet.label ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.tablet.label ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.tablet.label ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'tablet',
                                            'label',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>

                              <div
                                class="tab-pane fade"
                                id="multiselect-wrapper1"
                                role="tabpanel"
                                aria-labelledby="multiimage-wrapper-tab1"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">Wrapper width:</div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.tablet.wrapper ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.tablet.wrapper ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.tablet.wrapper ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'tablet',
                                            'wrapper',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </section>
                        <!-- Content for Tablet Tab -->
                      </div>

                      <!-- Desktop Tab -->
                      <div
                        class="tab-pane fade"
                        id="multiselect-desktop"
                        role="tabpanel"
                        aria-labelledby="multiimage-desktop-tab"
                      >
                        <!-- Content for Desktop Tab -->
                        <section>
                          <div
                            class="w-100 d-flex justify-content-between align-items-items-center py-3"
                          >
                            <div class="fs-14 text-64748B">DESKTOP</div>
                            <div class="text-xs fs-14 text-64748B">
                              Viewport size &gt;=1024px
                            </div>
                          </div>

                          <div class="w-100 py-3 tab-inner-content">
                            <ul
                              class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                              id="cont-tab2"
                              role="tablist"
                            >
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link active text-black tabFirst w-100"
                                  id="multiselect-container-tab2"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-container2"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-cont"
                                  aria-selected="true"
                                >
                                  Container
                                </button>
                              </li>
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link text-black tabCenter w-100"
                                  id="multiselect-label-tab2"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-label2"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-lebal"
                                  aria-selected="false"
                                >
                                  Label
                                </button>
                              </li>
                              <li class="nav-item" role="presentation">
                                <button
                                  class="nav-link text-black tablast w-100"
                                  id="multiselect-wrapper-tab2"
                                  data-bs-toggle="pill"
                                  data-bs-target="#multiselect-wrapper2"
                                  type="button"
                                  role="tab"
                                  aria-controls="pills-Wrapper"
                                  aria-selected="false"
                                >
                                  Wrapper
                                </button>
                              </li>
                            </ul>

                            <div class="tab-content" id="default-tabContent2">
                              <div
                                class="tab-pane fade show active"
                                id="multiselect-container2"
                                role="tabpanel"
                                aria-labelledby="multiimage-container-tab2"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">
                                        Container width:
                                      </div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.desktop.container ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.container ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.container ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'desktop',
                                            'container',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>

                              <div
                                class="tab-pane fade"
                                id="multiselect-label2"
                                role="tabpanel"
                                aria-labelledby="multiimage-label-tab2"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">Label width:</div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.desktop.label ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.label ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.label ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'desktop',
                                            'label',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>

                              <div
                                class="tab-pane fade"
                                id="multiselect-wrapper2"
                                role="tabpanel"
                                aria-labelledby="multiimage-wrapper-tab2"
                              >
                                <div class="w-100">
                                  <div class="mt-3">
                                    <div
                                      class="w-100 d-flex justify-content-between align-items-items-center"
                                    >
                                      <div class="fs-14 text-64748B">Wrapper width:</div>
                                      <div class="text-xs fs-14 text-64748B">1/12</div>
                                    </div>
                                    <div class="btn-group border w-100 mt-3">
                                      <button
                                        v-for="column in 12"
                                        :key="column"
                                        type="button"
                                        class="btn fs-12 bg-light h-100 px-1"
                                        :class="{
                                          activeBtnClass:
                                            targetElementColumns.desktop.wrapper ===
                                            `col-lg-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.wrapper ===
                                            `col-md-${column}`,
                                          activeBtnClass:
                                            targetElementColumns.desktop.wrapper ===
                                            `col-sm-${column}`,
                                        }"
                                        @click="
                                          setElementColumns(
                                            $event,
                                            'desktop',
                                            'wrapper',
                                            column
                                          )
                                        "
                                      >
                                        {{ column }}
                                      </button>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </section>
                        <!-- Content for Desktop Tab -->
                      </div>
                    </div>
                  </div>
                </div>
              </section>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Validation</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Field name </span
                  ><input
                    :value="targetElementData?.field_name"
                    @input="setMuiltiSelect($event, 'field_name')"
                    type="text"
                    placeholder="Default"
                    class="bg-input form-p-input-sm h-32"
                  />
                </div>
              </div>
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Required</span
                  >
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      :value="targetElementData?.required"
                      @change="setMuiltiSelect($event, 'required')"
                      role="switch"
                      id="flexSwitchCheckChecked"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Nullable</span
                  >
                  <div class="form-check form-switch">
                    <input
                      class="form-check-input"
                      :value="targetElementData?.nullable"
                      @input="setMuiltiSelect($event, 'nullable')"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                    /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>
              </div>
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center"
                >
                  <span class="fs-14 text-black">Min items</span
                  ><input
                    :value="targetElementData?.min_items"
                    @input="setMuiltiSelect($event, 'min_items')"
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                  />
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span class="fs-14 text-black">Max items</span
                  ><input
                    :value="targetElementData?.max_items"
                    @input="setMuiltiSelect($event, 'max_items')"
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                  />
                </div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span class="fs-14 text-black">Exact items</span
                  ><input
                    :value="targetElementData?.exact_items"
                    @input="setMuiltiSelect($event, 'exact_items')"
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                  />
                </div>
              </div>
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center"
                >
                  <span class="fs-14 text-black position-relative align-items-center"
                    >Additional rules
                    <a href="##" class="vfb-learn-more ms-2" target="_blank"
                      >learn more</a
                    ></span
                  >
                  <button
                    @click="addItem"
                    class="inline-block border-0 form-bg-primary form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                    role="button"
                    tabindex="0"
                  >
                    + Add
                  </button>
                  <!-- <button
                    @click="addRule"
                    + Add
                    </button> -->
                </div>

                <div class="vfb-faqs-body-inner border-0">
                  <div
                    v-for="(item, index) in items_AO"
                    :key="index"
                    class="add_inner position-relative"
                  >
                    <button
                      @click="removeItem(index, 'rules')"
                      :data="targetElementData?.rules"
                      class="close-svg-add-more-option border-0 p-0"
                    >
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 320 512"
                        fill="currentColor"
                      >
                        <path
                          data-v-c98426aa=""
                          d="M193.94 256L296.5 153.44l21.15-21.15c3.12-3.12 3.12-8.19 0-11.31l-22.63-22.63c-3.12-3.12-8.19-3.12-11.31 0L160 222.06 36.29 98.34c-3.12-3.12-8.19-3.12-11.31 0L2.34 120.97c-3.12 3.12-3.12 8.19 0 11.31L126.06 256 2.34 379.71c-3.12 3.12-3.12 8.19 0 11.31l22.63 22.63c3.12 3.12 8.19 3.12 11.31 0L160 289.94 262.56 392.5l21.15 21.15c3.12 3.12 8.19 3.12 11.31 0l22.63-22.63c3.12-3.12 3.12-8.19 0-11.31L193.94 256z"
                        ></path>
                      </svg>
                    </button>
                    <strong class="text-64748B mt-2 mb-1">AND</strong>
                    <select
                      class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                      v-model="item.type"
                      @change="handleTypeChange(index, 'rules')"
                      :data="targetElementData?.rules"
                    >
                      <option value="" selected disabled>Choose rule</option>
                      <option value="array">Array</option>
                      <option value="gt">Greater than</option>
                      <option value="gte">Greater than or equal</option>
                      <option value="lt">Less than</option>
                      <option value="lte">Less than or equal</option>
                    </select>
                    <select
                      v-if="item.type !== 'array'"
                      class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                      v-model="item.field"
                      @change="handleFieldChange(index, 'rules')"
                      :data="targetElementData?.rules"
                    >
                      <option value="" disabled>Other field</option>
                      <option v-for="(element, index) in getListOfElements" :key="index">
                        {{ element.identification }}
                      </option>
                    </select>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Conditions</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div class="vfb-faqs-body-inner">
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center"
                >
                  <span class="fs-14 text-black">The element has no conditions</span>
                  <div
                    @click="showModel($event)"
                    class="inline-block form-bg-primary form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                    id="validation.validation_wrapper.rules-add-button"
                    role="button"
                    tabindex="0"
                  >
                    + Edit
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Attributes</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div class="vfb-faqs-body-inner">
                <div class="d-flex justify-content-between">
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Custom attributes</span
                  >
                  <button
                    @click="addAttributes"
                    class="btn vf-primary text-white btn-sm rounded-2 text-sm fs-14"
                  >
                    Add
                  </button>
                </div>
                <div aria-labelledby="attributes.attrs__label">
                  <div
                    v-for="(attribute, key) in targetElementCustomAttributesArr"
                    :key="attribute.name"
                    class="d-flex align-items-center border-bottom checkclosehover position-relative mt-3"
                  >
                    <button
                      @click="removeElementCustomAttribute($event, key)"
                      class="close-svg-add-more-option border-0 p-0"
                    >
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 320 512"
                        fill="currentColor"
                      >
                        <path
                          d="M193.94 256L296.5 153.44l21.15-21.15c3.12-3.12 3.12-8.19 0-11.31l-22.63-22.63c-3.12-3.12-8.19-3.12-11.31 0L160 222.06 36.29 98.34c-3.12-3.12-8.19-3.12-11.31 0L2.34 120.97c-3.12 3.12-3.12 8.19 0 11.31L126.06 256 2.34 379.71c-3.12 3.12-3.12 8.19 0 11.31l22.63 22.63c3.12 3.12 8.19 3.12 11.31 0L160 289.94 262.56 392.5l21.15 21.15c3.12 3.12 8.19 3.12 11.31 0l22.63-22.63c3.12-3.12 3.12-8.19 0-11.31L193.94 256z"
                        />
                      </svg>
                    </button>
                    <input
                      type="text"
                      placeholder="Name"
                      :v-model="attribute.name"
                      class="add-more-option border-0 bg-transparent h-32 w-100 px-2 py-1 labelInput"
                    />
                    <span class="px-2">
                      <svg
                        class="vfb-icon cursor-pointer"
                        aria-hidden="true"
                        focusable="false"
                        role="img"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 448 512"
                      >
                        <path
                          class=""
                          fill="currentColor"
                          d="M311.03 131.515l-7.071 7.07c-4.686 4.686-4.686 12.284 0 16.971L387.887 239H12c-6.627 0-12 5.373-12 12v10c0 6.627 5.373 12 12 12h375.887l-83.928 83.444c-4.686 4.686-4.686 12.284 0 16.971l7.071 7.07c4.686 4.686 12.284 4.686 16.97 0l116.485-116c4.686-4.686 4.686-12.284 0-16.971L328 131.515c-4.686-4.687-12.284-4.687-16.97 0z"
                        />
                      </svg>
                    </span>
                    <input
                      @input="makeElementCustomAttribute($event)"
                      type="text"
                      placeholder="Value"
                      :v-model="attribute.value"
                      class="add-more-option border-0 bg-transparent px-2 py-1 h-32 w-100 valueInput"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- <Multi Image ------------------------------ Multi Image -->
  <div class="vfb-right-container" style="right: -500px" id="rightMenuMultiImage">
    <div class="position-relative h-100"></div>
    <div class="vfb-panels-wrapper-multiselect">
      <div class="vfb-config-panel-header-container">
        <div class="vfb-config-panel-header">
          <div class="vfb-config-panel-header-wrapper-left">
            <span
              class="vfb-config-panel-header-close"
              tabindex="0"
              @click="MultiClose"
              role="button"
              aria-label="Close config panel"
              ><svg
                class="vfb-icon vfb-config-panel-header-close-icon"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 320 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M207.6 256l107.72-107.72c6.23-6.23 6.23-16.34 0-22.58l-25.03-25.03c-6.23-6.23-16.34-6.23-22.58 0L160 208.4 52.28 100.68c-6.23-6.23-16.34-6.23-22.58 0L4.68 125.7c-6.23 6.23-6.23 16.34 0 22.58L112.4 256 4.68 363.72c-6.23 6.23-6.23 16.34 0 22.58l25.03 25.03c6.23 6.23 16.34 6.23 22.58 0L160 303.6l107.72 107.72c6.23 6.23 16.34 6.23 22.58 0l25.03-25.03c6.23-6.23 6.23-16.34 0-22.58L207.6 256z"
                ></path>
                <!--v-if-->
              </svg></span
            ><span id="multiselectname" class="vfb-config-panel-header-label">{{
              targetElementData?.identification
            }}</span>
          </div>
          <div class="vfb-config-panel-header-wrapper-right">
            <!-- Clone -->
            <div
              class="vfb-config-panel-header-clone"
              tabindex="0"
              role="button"
              aria-label="Clone"
              @click="cloneMultiFileElement"
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
                  d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zm-80 464c0 8.82-7.18 16-16 16H48c-8.82 0-16-7.18-16-16V144c0-8.82 7.18-16 16-16h48v240c0 26.51 21.49 48 48 48h240v48zm96-96c0 8.82-7.18 16-16 16H144c-8.82 0-16-7.18-16-16V48c0-8.82 7.18-16 16-16h320c8.82 0 16 7.18 16 16v320z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <!-- Remove -->
            <div
              class="vfb-config-panel-header-remove"
              tabindex="0"
              role="button"
              aria-label="Remove"
              @click="deleteElement"
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
                  d="M296 432h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zm-160 0h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zM440 64H336l-33.6-44.8A48 48 0 0 0 264 0h-80a48 48 0 0 0-38.4 19.2L112 64H8a8 8 0 0 0-8 8v16a8 8 0 0 0 8 8h24v368a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V96h24a8 8 0 0 0 8-8V72a8 8 0 0 0-8-8zM171.2 38.4A16.1 16.1 0 0 1 184 32h80a16.1 16.1 0 0 1 12.8 6.4L296 64H152zM384 464a16 16 0 0 1-16 16H80a16 16 0 0 1-16-16V96h320zm-168-32h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div
              class="vfb-config-panel-header-collapse vv-vfb-icon-plus"
              tabindex="0"
              role="button"
              aria-label="Expand all"
              @click="ColapsToggleExpand"
            >
              <svg
                class="vfb-icon vfb-config-panel-header-collapse-icon-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 206h-98v-98c0-6.6-5.4-12-12-12h-12c-6.6 0-12 5.4-12 12v98h-98c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h98v98c0 6.6 5.4 12 12 12h12c6.6 0 12-5.4 12-12v-98h98c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div
              class="vfb-config-panel-header-collapse d-none vv-vfb-icon-close"
              tabindex="0"
              role="button"
              aria-label="Collapse all"
              @click="ColapsToggleClose"
            >
              <svg
                class="vfb-icon vfb-config-panel-header-collapse-icon-close"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 242c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12H108c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h232z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Properties</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Name</span
                ><input
                  @change="setElementMultiImageAttribute($event, 'name')"
                  :value="targetElementData?.name"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input form-p-input-sm h-32"
                  value="multiImage"
                />
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Label</span
                ><textarea
                  @input="setElementMultiImageAttribute($event, 'label')"
                  :value="targetElementData?.label"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                  value="Multi-image"
                ></textarea>
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >Tooltip</span
                >
                <textarea
                  data-v-2a324127=""
                  type="text"
                  @input="setElementMultiImageAttribute($event, 'tooltip')"
                  :value="targetElementData?.tooltip"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                ></textarea>
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Description</span
                >
                <textarea
                  @input="setElementMultiImageAttribute($event, 'desc')"
                  :value="targetElementData?.desc"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                ></textarea>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Multi-file options</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Auto upload</span
                >
                <div class="form-check form-switch">
                  <input
                    class="form-check-input"
                    @change="autoUpload($event, 'autoupload')"
                    :value="targetElementData?.autoupload"
                    type="checkbox"
                    role="switch"
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >Drag & drop</span
                >
                <div class="form-check form-switch">
                  <input
                    class="form-check-input"
                    @change="autoUpload($event, 'dragdrop')"
                    :value="targetElementData?.dragdrop"
                    type="checkbox"
                    role="switch"
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >Soft remove</span
                >
                <div class="form-check form-switch">
                  <input
                    class="form-check-input"
                    @change="autoUpload($event, 'softremove')"
                    :value="targetElementData?.softremove"
                    type="checkbox"
                    role="switch"
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Clickable
                </span>
                <div class="form-check form-switch">
                  <input
                    class="form-check-input"
                    @change="autoUpload($event, 'clickable')"
                    :value="targetElementData?.softremove"
                    type="checkbox"
                    role="switch"
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div class="fs-14 text-64748B medium">URLS</div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >Click URL
                </span>
                <input
                  @input="setElementMultiImageAttribute($event, 'click_urls')"
                  :value="targetElementData?.click_urls"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-start mt-2"
              >
                <span
                  class="fs-14 form-text-Inner text-black position-relative d-flex align-items-center form-bg-info"
                  >Preview
                  <br />
                  URL</span
                >
                <input
                  data-v-2a324127=""
                  @input="setElementMultiImageAttribute($event, 'preview_urls')"
                  :value="targetElementData?.preview_urls"
                  type="text"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div class="fs-14 text-64748B medium">CONTROLS</div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Can add</span
                >
                <div class="form-check form-switch">
                  <input
                    @change="autoUpload($event, 'control_can_add')"
                    :value="targetElementData?.control_can_add"
                    class="form-check-input"
                    type="checkbox"
                    role="switch"
                    id="flexSwitchCheckChecked"
                    checked
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Can remove</span
                >
                <div class="form-check form-switch">
                  <input
                    @change="autoUpload($event, 'control_can_remove')"
                    :value="targetElementData?.control_can_remove"
                    class="form-check-input"
                    type="checkbox"
                    role="switch"
                    id="flexSwitchCheckChecked"
                    checked
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Can sort</span
                >
                <div class="form-check form-switch">
                  <input
                    @change="autoUpload($event, 'control_can_sort')"
                    :value="targetElementData?.control_can_sort"
                    class="form-check-input"
                    type="checkbox"
                    role="switch"
                    id="flexSwitchCheckChecked"
                    checked
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div class="fs-14 text-64748B medium">STORE FORMAT</div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Store value in object
                </span>
                <div class="form-check form-switch d-none">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    role="switch"
                    id="flexSwitchCheckChecked"
                    checked
                  />
                  <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >File key</span
                >
                <textarea
                  data-v-2a324127=""
                  type="text"
                  @input="setElementMultiImageAttribute($event, 'file_key')"
                  :value="targetElementData?.file_key"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                ></textarea>
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div class="fs-14 text-64748B medium">ACCEPT</div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center px-0 vfb-faqs-body-inner border-0"
                data-v-2a324127=""
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center"
                  data-v-2a324127=""
                  >Size</span
                >
                <div class="btn-group vfb_multiimage_btn border" data-v-2a324127="">
                  <button
                    @click="setAccept($event, 'accetptedvalues', 'audio/*')"
                    :value="targetElementData?.accetptedvalues"
                    defaultvalue="audio/*"
                    class="btn fs-12 h-100 px-2"
                    checked="false"
                  >
                    Audio
                  </button>
                  <button
                    @click="setAccept($event, 'accetptedvalues', 'video/*')"
                    :value="targetElementData?.accetptedvalues"
                    defaultvalue="video/*"
                    class="btn fs-12 h-100 px-2"
                    checked="false"
                  >
                    Video
                  </button>
                  <button
                    @click="setAccept($event, 'accetptedvalues', 'image/*')"
                    :value="targetElementData?.accetptedvalues"
                    defaultvalue="image/*"
                    class="btn fs-12 h-100 px-2"
                    checked="false"
                  >
                    image
                  </button>
                </div>
              </div>
            </div>
            <div class="vfb-faqs-body-inner d-none">
              <div class="fs-14 text-64748B medium">ENDPOINTS</div>
              <div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-3"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Upload temp
                  </span>
                </div>
                <div class="d-flex pt-2">
                  <div class="d-flex form-border-width-input bg-input px-2 me-2 h-32">
                    <span class="px-2">
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
                          d="M301.148 394.702l-79.2 79.19c-50.778 50.799-133.037 50.824-183.84 0-50.799-50.778-50.824-133.037 0-183.84l79.19-79.2a132.833 132.833 0 0 1 3.532-3.403c7.55-7.005 19.795-2.004 20.208 8.286.193 4.807.598 9.607 1.216 14.384.481 3.717-.746 7.447-3.397 10.096-16.48 16.469-75.142 75.128-75.3 75.286-36.738 36.759-36.731 96.188 0 132.94 36.759 36.738 96.188 36.731 132.94 0l79.2-79.2.36-.36c36.301-36.672 36.14-96.07-.37-132.58-8.214-8.214-17.577-14.58-27.585-19.109-4.566-2.066-7.426-6.667-7.134-11.67a62.197 62.197 0 0 1 2.826-15.259c2.103-6.601 9.531-9.961 15.919-7.28 15.073 6.324 29.187 15.62 41.435 27.868 50.688 50.689 50.679 133.17 0 183.851zm-90.296-93.554c12.248 12.248 26.362 21.544 41.435 27.868 6.388 2.68 13.816-.68 15.919-7.28a62.197 62.197 0 0 0 2.826-15.259c.292-5.003-2.569-9.604-7.134-11.67-10.008-4.528-19.371-10.894-27.585-19.109-36.51-36.51-36.671-95.908-.37-132.58l.36-.36 79.2-79.2c36.752-36.731 96.181-36.738 132.94 0 36.731 36.752 36.738 96.181 0 132.94-.157.157-58.819 58.817-75.3 75.286-2.651 2.65-3.878 6.379-3.397 10.096a163.156 163.156 0 0 1 1.216 14.384c.413 10.291 12.659 15.291 20.208 8.286a131.324 131.324 0 0 0 3.532-3.403l79.19-79.2c50.824-50.803 50.799-133.062 0-183.84-50.802-50.824-133.062-50.799-183.84 0l-79.2 79.19c-50.679 50.682-50.688 133.163 0 183.851z"
                        ></path>
                        <!--v-if-->
                      </svg>
                    </span>
                    <input
                      type="text"
                      class="border-0 bg-transparent w-100"
                      name=""
                      id=""
                      placeholder="Default"
                    />
                  </div>
                  <div class="vfb_select">
                    <select class="form-select h-32 bg-input" aria-label="Default select">
                      <option value="0" disabled>Method</option>
                      <option value="1" selected>Default</option>
                      <option value="2">POST</option>
                      <option value="3">GET</option>
                      <option value="3">PULL</option>
                      <option value="3">PATCH</option>
                    </select>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-3"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Remove temp
                  </span>
                </div>
                <div class="d-flex pt-2">
                  <div class="d-flex form-border-width-input bg-input px-2 me-2 h-32">
                    <span class="px-2">
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
                          d="M301.148 394.702l-79.2 79.19c-50.778 50.799-133.037 50.824-183.84 0-50.799-50.778-50.824-133.037 0-183.84l79.19-79.2a132.833 132.833 0 0 1 3.532-3.403c7.55-7.005 19.795-2.004 20.208 8.286.193 4.807.598 9.607 1.216 14.384.481 3.717-.746 7.447-3.397 10.096-16.48 16.469-75.142 75.128-75.3 75.286-36.738 36.759-36.731 96.188 0 132.94 36.759 36.738 96.188 36.731 132.94 0l79.2-79.2.36-.36c36.301-36.672 36.14-96.07-.37-132.58-8.214-8.214-17.577-14.58-27.585-19.109-4.566-2.066-7.426-6.667-7.134-11.67a62.197 62.197 0 0 1 2.826-15.259c2.103-6.601 9.531-9.961 15.919-7.28 15.073 6.324 29.187 15.62 41.435 27.868 50.688 50.689 50.679 133.17 0 183.851zm-90.296-93.554c12.248 12.248 26.362 21.544 41.435 27.868 6.388 2.68 13.816-.68 15.919-7.28a62.197 62.197 0 0 0 2.826-15.259c.292-5.003-2.569-9.604-7.134-11.67-10.008-4.528-19.371-10.894-27.585-19.109-36.51-36.51-36.671-95.908-.37-132.58l.36-.36 79.2-79.2c36.752-36.731 96.181-36.738 132.94 0 36.731 36.752 36.738 96.181 0 132.94-.157.157-58.819 58.817-75.3 75.286-2.651 2.65-3.878 6.379-3.397 10.096a163.156 163.156 0 0 1 1.216 14.384c.413 10.291 12.659 15.291 20.208 8.286a131.324 131.324 0 0 0 3.532-3.403l79.19-79.2c50.824-50.803 50.799-133.062 0-183.84-50.802-50.824-133.062-50.799-183.84 0l-79.2 79.19c-50.679 50.682-50.688 133.163 0 183.851z"
                        ></path>
                        <!--v-if-->
                      </svg>
                    </span>
                    <input
                      type="text"
                      class="border-0 bg-transparent w-100"
                      name=""
                      id=""
                      placeholder="Default"
                    />
                  </div>
                  <div class="vfb_select">
                    <select class="form-select h-32 bg-input" aria-label="Default select">
                      <option value="0" disabled>Method</option>
                      <option value="1" selected>Default</option>
                      <option value="2">POST</option>
                      <option value="3">GET</option>
                      <option value="3">PULL</option>
                      <option value="3">PATCH</option>
                    </select>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="form-text-sm d-flex justify-content-between align-items-center mt-3"
                >
                  <span
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Remove
                  </span>
                </div>
                <div class="d-flex pt-2">
                  <div class="d-flex form-border-width-input bg-input px-2 me-2 h-32">
                    <span class="px-2">
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
                          d="M301.148 394.702l-79.2 79.19c-50.778 50.799-133.037 50.824-183.84 0-50.799-50.778-50.824-133.037 0-183.84l79.19-79.2a132.833 132.833 0 0 1 3.532-3.403c7.55-7.005 19.795-2.004 20.208 8.286.193 4.807.598 9.607 1.216 14.384.481 3.717-.746 7.447-3.397 10.096-16.48 16.469-75.142 75.128-75.3 75.286-36.738 36.759-36.731 96.188 0 132.94 36.759 36.738 96.188 36.731 132.94 0l79.2-79.2.36-.36c36.301-36.672 36.14-96.07-.37-132.58-8.214-8.214-17.577-14.58-27.585-19.109-4.566-2.066-7.426-6.667-7.134-11.67a62.197 62.197 0 0 1 2.826-15.259c2.103-6.601 9.531-9.961 15.919-7.28 15.073 6.324 29.187 15.62 41.435 27.868 50.688 50.689 50.679 133.17 0 183.851zm-90.296-93.554c12.248 12.248 26.362 21.544 41.435 27.868 6.388 2.68 13.816-.68 15.919-7.28a62.197 62.197 0 0 0 2.826-15.259c.292-5.003-2.569-9.604-7.134-11.67-10.008-4.528-19.371-10.894-27.585-19.109-36.51-36.51-36.671-95.908-.37-132.58l.36-.36 79.2-79.2c36.752-36.731 96.181-36.738 132.94 0 36.731 36.752 36.738 96.181 0 132.94-.157.157-58.819 58.817-75.3 75.286-2.651 2.65-3.878 6.379-3.397 10.096a163.156 163.156 0 0 1 1.216 14.384c.413 10.291 12.659 15.291 20.208 8.286a131.324 131.324 0 0 0 3.532-3.403l79.19-79.2c50.824-50.803 50.799-133.062 0-183.84-50.802-50.824-133.062-50.799-183.84 0l-79.2 79.19c-50.679 50.682-50.688 133.163 0 183.851z"
                        ></path>
                        <!--v-if-->
                      </svg>
                    </span>
                    <input
                      type="text"
                      class="border-0 bg-transparent w-100"
                      name=""
                      id=""
                      placeholder="Default"
                    />
                  </div>
                  <div class="vfb_select">
                    <select
                      class="form-select h-32 bg-input"
                      aria-label="Default select"
                      placeholder="Default"
                    >
                      <option value="0" disabled>Method</option>
                      <option value="1">Default</option>
                      <option value="2">POST</option>
                      <option value="3">GET</option>
                      <option value="3">PULL</option>
                      <option value="3">PATCH</option>
                    </select>
                  </div>
                </div>
              </div>
            </div>
            <div class="vfb-faqs-body-inner d-none">
              <div class="fs-14 text-64748B medium">REQUEST PARAMS</div>
              <div
                data-v-7ebfecff=""
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between mt-3"
              >
                <span
                  data-v-7ebfecff=""
                  class="fs-14 text-black position-relative d-flex form-bg-info align-items-center"
                  data-v-2a324127=""
                  >Custom attributes</span
                >
                <div
                  data-v-7ebfecff=""
                  class="inline-block form-bg-primary form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                  id="validation.validation_wrapper.rules-add-button"
                  role="button"
                  tabindex="0"
                >
                  + Add
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Data</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span class="fs-14 text-black position-relative d-flex align-items-center"
                  >Submit data</span
                >
                <div class="form-check form-switch">
                  <input
                    @change="autoUpload($event, 'submit_data')"
                    :value="targetElementData?.submit_data"
                    class="form-check-input"
                    type="checkbox"
                    role="switch"
                    id="flexSwitchCheckChecked"
                    checked
                  /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Decorators</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Before</span
                ><input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementMultiImageAttribute($event, 'before')"
                  :value="targetElementData?.before"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Between</span
                ><input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementMultiImageAttribute($event, 'between')"
                  :value="targetElementData?.between"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>

              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span data-v-2a324127="" class="fs-14 text-black">After</span
                ><input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementMultiImageAttribute($event, 'after')"
                  :value="targetElementData?.after"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Layout</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div
              class="form-text-sm d-none justify-content-between align-items-baseline vfb-faqs-body-inner border-bottom-0"
              data-v-2a324127=""
            >
              <span
                class="fs-14 text-black position-relative d-flex align-items-center"
                data-v-2a324127=""
                >View
                <a
                  href="##"
                  class="vfb-learn-more ms-2"
                  target="_blank"
                  data-v-2a324127=""
                  >learn more</a
                ></span
              >
              <div class="btn-group border" data-v-2a324127="">
                <button
                  type="button"
                  class="btn fs-12 vf-primary text-white h-100 px-3"
                  data-v-2a324127=""
                >
                  File</button
                ><button
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  Image</button
                ><button
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  Gallery
                </button>
              </div>
            </div>
            <div
              class="form-text-sm d-flex justify-content-between align-items-center vfb-faqs-body-inner border-bottom-0"
            >
              <span class="fs-14 text-black position-relative d-flex align-items-center"
                >Size
                <a href="##" class="vfb-learn-more ms-2" target="_blank"
                  >learn more</a
                ></span
              >
              <div class="btn-group border">
                <button
                  @click="setElementSizeAttributeImage($event, 'size', 'font-default')"
                  type="button"
                  class="btn fs-12 h-100 px-2"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-default',
                  }"
                >
                  Default</button
                ><button
                  @click="setElementSizeAttributeImage($event, 'size', 'font-sm')"
                  type="button"
                  class="btn fs-12 border-start px-3"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-sm',
                  }"
                >
                  sm</button
                ><button
                  @click="setElementSizeAttributeImage($event, 'size', 'font-md')"
                  type="button"
                  class="btn fs-12 border-start px-3"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-md',
                  }"
                >
                  md</button
                ><button
                  @click="setElementSizeAttributeImage($event, 'size', 'font-lg')"
                  type="button"
                  class="btn fs-12 border-start px-3"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-lg',
                  }"
                >
                  lg
                </button>
              </div>
            </div>

            <section class="text-layout">
              <div
                class="form-text-sm d-flex flex-wrap justify-content-between align-items-center mt-2 vfb-faqs-body-inner border-bottom-0"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                >
                  Columns
                  <a href="#" class="vfb-learn-more ms-2" target="_blank">learn more</a>
                </span>
                <div class="w-100 py-2">
                  <ul
                    class="nav nav-pills border category_tabs container_tabs"
                    id="multiimage-tab"
                    role="tablist"
                  >
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link active text-black tabFirst w-100"
                        id="multiimage-default-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#multiimage-default"
                        type="button"
                        role="tab"
                        aria-controls="select-default"
                        aria-selected="true"
                      >
                        Default
                      </button>
                    </li>
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link text-black tabCenter w-100"
                        id="multiimage-tablet-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#multiimage-tablet"
                        type="button"
                        role="tab"
                        aria-controls="select-tablet"
                        aria-selected="false"
                      >
                        Tablet
                      </button>
                    </li>
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link text-black tablast w-100"
                        id="multiimage-desktop-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#multiimage-desktop"
                        type="button"
                        role="tab"
                        aria-controls="select-desktop"
                        aria-selected="false"
                      >
                        Desktop
                      </button>
                    </li>
                  </ul>

                  <div class="tab-content">
                    <!-- Default Tab -->
                    <div
                      class="tab-pane fade show active"
                      id="multiimage-default"
                      role="tabpanel"
                      aria-labelledby="multiimage-default-tab"
                    >
                      <!-- Content for Default Tab -->
                      <section>
                        <div
                          class="w-100 d-flex justify-content-between align-items-items-center py-3"
                        >
                          <div class="fs-14 text-64748B">DEFAULT</div>
                          <div class="text-xs fs-14 text-64748B">
                            Viewport size &gt;=0px
                          </div>
                        </div>

                        <div class="w-100 py-3 tab-inner-content">
                          <ul
                            class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                            id="cont-tab"
                            role="tablist"
                          >
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link active text-black tabFirst w-100"
                                id="multiimage-container-tab"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-container"
                                type="button"
                                role="tab"
                                aria-controls="pills-cont"
                                aria-selected="true"
                              >
                                Container
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tabCenter w-100"
                                id="multiimage-label-tab"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-label"
                                type="button"
                                role="tab"
                                aria-controls="pills-lebal"
                                aria-selected="false"
                              >
                                Label
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tablast w-100"
                                id="multiimage-wrapper-tab"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-wrapper"
                                type="button"
                                role="tab"
                                aria-controls="pills-Wrapper"
                                aria-selected="false"
                              >
                                Wrapper
                              </button>
                            </li>
                          </ul>

                          <div class="tab-content" id="default-tabContent">
                            <div
                              class="tab-pane fade show active"
                              id="multiimage-container"
                              role="tabpanel"
                              aria-labelledby="multiimage-container-tab"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Container width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.default.container ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.container ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.container ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'default',
                                          'container',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="multiimage-label"
                              role="tabpanel"
                              aria-labelledby="multiimage-label-tab"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Label width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.default.label ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.label ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.label ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'default',
                                          'label',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="multiimage-wrapper"
                              role="tabpanel"
                              aria-labelledby="multiimage-wrapper-tab"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Wrapper width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.default.wrapper ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.wrapper ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.wrapper ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'default',
                                          'wrapper',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </section>
                      <!-- Content for Default Tab -->
                    </div>

                    <!-- Tablet Tab -->
                    <div
                      class="tab-pane fade"
                      id="multiimage-tablet"
                      role="tabpanel"
                      aria-labelledby="multiimage-tablet-tab"
                    >
                      <!-- Content for Tablet Tab -->
                      <section>
                        <div
                          class="w-100 d-flex justify-content-between align-items-items-center py-3"
                        >
                          <div class="fs-14 text-64748B">TABLET</div>
                          <div class="text-xs fs-14 text-64748B">
                            Viewport size &gt;=640px
                          </div>
                        </div>

                        <div class="w-100 py-3 tab-inner-content">
                          <ul
                            class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                            id="cont-tab1"
                            role="tablist"
                          >
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link active text-black tabFirst w-100"
                                id="multiimage-container-tab1"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-container1"
                                type="button"
                                role="tab"
                                aria-controls="pills-cont"
                                aria-selected="true"
                              >
                                Container
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tabCenter w-100"
                                id="multiimage-label-tab1"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-label1"
                                type="button"
                                role="tab"
                                aria-controls="pills-lebal"
                                aria-selected="false"
                              >
                                Label
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tablast w-100"
                                id="multiimage-wrapper-tab1"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-wrapper1"
                                type="button"
                                role="tab"
                                aria-controls="pills-Wrapper"
                                aria-selected="false"
                              >
                                Wrapper
                              </button>
                            </li>
                          </ul>

                          <div class="tab-content" id="default-tabContent1">
                            <div
                              class="tab-pane fade show active"
                              id="multiimage-container1"
                              role="tabpanel"
                              aria-labelledby="multiimage-container-tab1"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Container width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'container',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="multiimage-label1"
                              role="tabpanel"
                              aria-labelledby="multiimage-label-tab1"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Label width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.tablet.label ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.label ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.label ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'tablet',
                                          'label',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="multiimage-wrapper1"
                              role="tabpanel"
                              aria-labelledby="multiimage-wrapper-tab1"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Wrapper width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.tablet.wrapper ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.wrapper ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.wrapper ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'tablet',
                                          'wrapper',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </section>
                      <!-- Content for Tablet Tab -->
                    </div>

                    <!-- Desktop Tab -->
                    <div
                      class="tab-pane fade"
                      id="multiimage-desktop"
                      role="tabpanel"
                      aria-labelledby="multiimage-desktop-tab"
                    >
                      <!-- Content for Desktop Tab -->
                      <section>
                        <div
                          class="w-100 d-flex justify-content-between align-items-items-center py-3"
                        >
                          <div class="fs-14 text-64748B">DESKTOP</div>
                          <div class="text-xs fs-14 text-64748B">
                            Viewport size &gt;=1024px
                          </div>
                        </div>

                        <div class="w-100 py-3 tab-inner-content">
                          <ul
                            class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                            id="cont-tab2"
                            role="tablist"
                          >
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link active text-black tabFirst w-100"
                                id="multiimage-container-tab2"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-container2"
                                type="button"
                                role="tab"
                                aria-controls="pills-cont"
                                aria-selected="true"
                              >
                                Container
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tabCenter w-100"
                                id="multiimage-label-tab2"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-label2"
                                type="button"
                                role="tab"
                                aria-controls="pills-lebal"
                                aria-selected="false"
                              >
                                Label
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tablast w-100"
                                id="multiimage-wrapper-tab2"
                                data-bs-toggle="pill"
                                data-bs-target="#multiimage-wrapper2"
                                type="button"
                                role="tab"
                                aria-controls="pills-Wrapper"
                                aria-selected="false"
                              >
                                Wrapper
                              </button>
                            </li>
                          </ul>

                          <div class="tab-content" id="default-tabContent2">
                            <div
                              class="tab-pane fade show active"
                              id="multiimage-container2"
                              role="tabpanel"
                              aria-labelledby="multiimage-container-tab2"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Container width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'container',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="multiimage-label2"
                              role="tabpanel"
                              aria-labelledby="multiimage-label-tab2"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Label width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.label ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.label ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.label ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'label',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="multiimage-wrapper2"
                              role="tabpanel"
                              aria-labelledby="multiimage-wrapper-tab2"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Wrapper width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.wrapper ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.wrapper ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.wrapper ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'wrapper',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </section>
                      <!-- Content for Desktop Tab -->
                    </div>
                  </div>
                </div>
              </div>
            </section>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Validation</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner" data-v-7ebfecff="">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center"
                data-v-7ebfecff=""
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  data-v-7ebfecff=""
                  >Field name</span
                ><input
                  data-v-2a324127=""
                  type="text"
                  placeholder="Default"
                  @input="setElementMultiImageAttribute($event, 'field_name')"
                  :value="targetElementData?.field_name"
                  class="bg-input form-p-input-sm h-32"
                  data-v-7ebfecff=""
                />
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Min file size</span
                >
                <div
                  class="vfb_form_fonts vfb_multiImage_form d-flex justify-content-end position-relative"
                >
                  <input
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                    @input="setElementMultiImageAttribute($event, 'min_file_size')"
                    :value="targetElementData?.min_file_size"
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">KB</p>
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Max file size</span
                >
                <div
                  class="vfb_form_fonts vfb_multiImage_form d-flex justify-content-end position-relative"
                >
                  <input
                    class="form-control w-50 bg-input"
                    type="number"
                    @input="setElementMultiImageAttribute($event, 'max_file_size')"
                    :value="targetElementData?.max_file_size"
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">KB</p>
                </div>
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >MIME types</span
                >
                <div class="border rounded px-2 py-2 position-relative">
                  <ul class="ps-0 mb-0">
                    <li v-for="(tag, index) in tags" :key="index" class="tag">
                      {{ tag }}
                      <button
                        class="bg-transparent border-0 bg-transparent text-white"
                        :value="targetElementData?.mimi_type"
                        @click="removeTag(index, 'mimi_types')"
                      >
                        x
                      </button>
                    </li>
                  </ul>

                  <!-- Multi-tag input field -->
                  <div>
                    <input
                      :id="'conditions.' + index + '.conditions.' + index + '.groups'"
                      class="border-0 bg-transparent"
                      v-model="tagInput"
                      :data="targetElementData?.mimi_type"
                      @click="checkDisplay($event)"
                      @keydown.enter.prevent="addTag($event, 'mimi_types')"
                      placeholder="Accepted values"
                    />
                  </div>

                  <!-- List for multi-tags -->
                  <ul class="ps-0 mb-0 tagsMultiSelect" style="display: none">
                    <li
                      v-for="tagOption in tagOptions"
                      :key="tagOption"
                      :value="targetElementData?.mimi_type"
                      @click="addTagOption(tagOption, 'mimi_types')"
                      class="tag-option"
                    >
                      {{ tagOption }}
                    </li>
                  </ul>
                </div>

                <div
                  class="vfb_form_fonts vfb_multiImage_select d-none justify-content-end position-relative"
                ></div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Extensions</span
                >
                <div class="border rounded px-2 py-2 position-relative">
                  <ul class="ps-0 mb-0">
                    <li v-for="(tag, index) in tags2" :key="index" class="tag">
                      {{ tag }}
                      <button
                        class="bg-transparent border-0 bg-transparent text-white"
                        :value="targetElementData?.extensions"
                        @click="removeTag2(index, 'extensions')"
                      >
                        x
                      </button>
                    </li>
                  </ul>

                  <!-- Multi-tag input field -->
                  <div>
                    <input
                      :id="'conditions2.' + index + '.conditions2.' + index + '.groups2'"
                      class="border-0 bg-transparent"
                      v-model="tagInput2"
                      :data="targetElementData?.extensions"
                      @click="checkDisplay2($event)"
                      @keydown.enter.prevent="addTag2($event, 'extensions')"
                      placeholder="Accepted values"
                    />
                  </div>

                  <!-- List for multi-tags -->
                  <ul class="ps-0 mb-0 tagsMultiSelect" style="display: none">
                    <li
                      v-for="tagOption in tagOptions2"
                      :key="tagOption"
                      :value="targetElementData?.extensions"
                      @click="addTagOption2(tagOption, 'extensions')"
                      class="tag-option"
                    >
                      {{ tagOption }}
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div class="fs-14 text-64748B medium">DIMENSIONS</div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Width</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementMultiImageAttribute($event, 'width')"
                    :value="targetElementData?.width"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Height</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementMultiImageAttribute($event, 'height')"
                    :value="targetElementData?.height"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Min width</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementMultiImageAttribute($event, 'min_width')"
                    :value="targetElementData?.min_width"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Min Height</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementMultiImageAttribute($event, 'min_height')"
                    :value="targetElementData?.min_height"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Max width</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementMultiImageAttribute($event, 'max_width')"
                    :value="targetElementData?.max_width"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Max Height</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementMultiImageAttribute($event, 'max_height')"
                    :value="targetElementData?.max_height"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                data-v-7ebfecff=""
              >
                <span data-v-2a324127="" class="fs-14 text-black" data-v-7ebfecff=""
                  >Ratio</span
                ><input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementMultiImageAttribute($event, 'ratio')"
                  :value="targetElementData?.ratio"
                  placeholder="eg. 2/3 or 0.66"
                  class="bg-input form-p-input-sm h-32"
                  data-v-7ebfecff=""
                />
              </div>
            </div>
            <div class="vfb-faqs-body-inner" data-v-7ebfecff="">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >Required</span
                >
                <div data-v-2a324127="" class="form-check form-switch">
                  <input
                    data-v-2a324127=""
                    class="form-check-input"
                    type="checkbox"
                    role="switch"
                    id="flexSwitchCheckChecked"
                    @input="setElementMultiImageAttribute($event, 'required')"
                    :value="targetElementData?.required"
                  /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >Nullable</span
                >
                <div data-v-2a324127="" class="form-check form-switch">
                  <input
                    data-v-2a324127=""
                    class="form-check-input"
                    type="checkbox"
                    @input="setElementMultiImageAttribute($event, 'nullable')"
                    :value="targetElementData?.nullable"
                    role="switch"
                    id="flexSwitchCheckChecked"
                  /><!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                </div>
              </div>
            </div>

            <div class="vfb-faqs-body-inner" data-v-7ebfecff="">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center"
                data-v-7ebfecff=""
              >
                <span data-v-2a324127="" class="fs-14 text-black" data-v-7ebfecff=""
                  >Min items</span
                ><input
                  data-v-2a324127=""
                  type="number"
                  @input="setElementMultiImageAttribute($event, 'min_items')"
                  :value="targetElementData?.min_items"
                  class="bg-input form-p-input-sm h-32"
                  data-v-7ebfecff=""
                />
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                data-v-7ebfecff=""
              >
                <span data-v-2a324127="" class="fs-14 text-black" data-v-7ebfecff=""
                  >Max items</span
                ><input
                  data-v-2a324127=""
                  type="number"
                  @input="setElementMultiImageAttribute($event, 'max_items')"
                  :value="targetElementData?.max_items"
                  class="bg-input form-p-input-sm h-32"
                  data-v-7ebfecff=""
                />
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                data-v-7ebfecff=""
              >
                <span data-v-2a324127="" class="fs-14 text-black" data-v-7ebfecff=""
                  >Exact Items</span
                ><input
                  data-v-2a324127=""
                  type="number"
                  @input="setElementMultiImageAttribute($event, 'exact_items')"
                  :value="targetElementData?.exact_items"
                  class="bg-input form-p-input-sm h-32"
                  data-v-7ebfecff=""
                />
              </div>
            </div>

            <div class="vfb-faqs-body-inner">
              <div class="form-text-sm d-flex justify-content-between align-items-center">
                <span class="fs-14 text-black position-relative align-items-center"
                  >Additional rules
                  <a href="##" class="vfb-learn-more ms-2" target="_blank"
                    >learn more</a
                  ></span
                >
                <button
                  @click="addItem"
                  class="inline-block border-0 form-bg-primary form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                  role="button"
                  tabindex="0"
                >
                  + Add
                </button>
                <!-- <button
                    @click="addRule"
                    + Add
                    </button> -->
              </div>

              <div class="vfb-faqs-body-inner border-0">
                <div
                  v-for="(item, index) in items_AO"
                  :key="index"
                  class="add_inner position-relative"
                >
                  <button
                    @click="removeItem(index, 'rules')"
                    :data="targetElementData?.rules"
                    class="close-svg-add-more-option border-0 p-0"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 320 512"
                      fill="currentColor"
                    >
                      <path
                        data-v-c98426aa=""
                        d="M193.94 256L296.5 153.44l21.15-21.15c3.12-3.12 3.12-8.19 0-11.31l-22.63-22.63c-3.12-3.12-8.19-3.12-11.31 0L160 222.06 36.29 98.34c-3.12-3.12-8.19-3.12-11.31 0L2.34 120.97c-3.12 3.12-3.12 8.19 0 11.31L126.06 256 2.34 379.71c-3.12 3.12-3.12 8.19 0 11.31l22.63 22.63c3.12 3.12 8.19 3.12 11.31 0L160 289.94 262.56 392.5l21.15 21.15c3.12 3.12 8.19 3.12 11.31 0l22.63-22.63c3.12-3.12 3.12-8.19 0-11.31L193.94 256z"
                      ></path>
                    </svg>
                  </button>
                  <strong class="text-64748B mt-2 mb-1">AND</strong>
                  <select
                    class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                    v-model="item.type"
                    @change="handleTypeChange(index, 'rules')"
                    :data="targetElementData?.rules"
                  >
                    <option value="" selected disabled>Choose rule</option>
                    <option value="array">Array</option>
                    <option value="gt">Greater than</option>
                    <option value="gte">Greater than or equal</option>
                    <option value="lt">Less than</option>
                    <option value="lte">Less than or equal</option>
                  </select>
                  <select
                    v-if="item.type !== 'array'"
                    class="form-select bg-input w-100 border-0 ps-3 bg-transparent rounded-0 border-bottom"
                    v-model="item.field"
                    @change="handleFieldChange(index, 'rules')"
                    :data="targetElementData?.rules"
                  >
                    <option value="" disabled>Other field</option>
                    <option v-for="(element, index) in getListOfElements" :key="index">
                      {{ element.identification }}
                    </option>
                  </select>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Conditions</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm vfb_element_section d-flex justify-content-between align-items-center"
              >
                <span data-v-2a324127="" class="fs-14 text-black"
                  >The element has no conditions</span
                >
                <!-- Button trigger modal -->
                <button
                  @click="showModel($event)"
                  type="button"
                  class="btn text-white vfb_model_condition"
                >
                  Edit
                </button>
              </div>
            </div>
          </div>
        </div>
        <div class="vfb-faqs">
          <div class="vfb-faqs-item">
            <div
              @click="handleClick"
              class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
            >
              <span class="medium text-black">Attributes</span>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  fill="#94a3b8"
                  d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
              <svg
                width="12px"
                height="12px"
                class="vfb-icon vfb-config-form-header-collapse-close d-none"
                aria-hidden="true"
                focusable="false"
                fill="#94a3b8"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 384 512"
              >
                <path
                  class=""
                  d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div class="vfb-faqs-body bg-white" style="display: none">
              <div data-v-7ebfecff="" class="vfb-faqs-body-inner">
                <div
                  data-v-7ebfecff=""
                  data-v-2a324127=""
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                >
                  <span
                    data-v-7ebfecff=""
                    data-v-2a324127=""
                    class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                    >Disabled</span
                  >
                  <div
                    data-v-7ebfecff=""
                    data-v-2a324127=""
                    class="form-check form-switch"
                  >
                    <input
                      data-v-7ebfecff=""
                      data-v-2a324127=""
                      @change="autoUpload($event, 'disabled')"
                      :value="targetElementData?.disabled"
                      class="form-check-input"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckChecked"
                    />
                    <!-- <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label> -->
                  </div>
                </div>

                <div
                  data-v-2a324127=""
                  class="form-text-sm d-flex justify-content-between align-items-center mt-2"
                  data-v-7ebfecff=""
                >
                  <span data-v-2a324127="" class="fs-14 text-black" data-v-7ebfecff=""
                    >ID</span
                  ><input
                    @input="setElementMultiImageAttribute($event, 'inputId')"
                    :value="targetElementData?.inputId"
                    data-v-2a324127=""
                    type="text"
                    class="bg-input form-p-input-sm h-32"
                    data-v-7ebfecff=""
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!--  Image ------------------------------ Image -->
  <div class="vfb-right-container" style="right: -500px" id="rightMenuImage">
    <div class="position-relative h-100"></div>
    <div class="vfb-panels-wrapper-multiselect">
      <div class="vfb-config-panel-header-container">
        <div class="vfb-config-panel-header">
          <div class="vfb-config-panel-header-wrapper-left">
            <span
              class="vfb-config-panel-header-close"
              tabindex="0"
              @click="ImageClose"
              role="button"
              aria-label="Close config panel"
              ><svg
                class="vfb-icon vfb-config-panel-header-close-icon"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 320 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M207.6 256l107.72-107.72c6.23-6.23 6.23-16.34 0-22.58l-25.03-25.03c-6.23-6.23-16.34-6.23-22.58 0L160 208.4 52.28 100.68c-6.23-6.23-16.34-6.23-22.58 0L4.68 125.7c-6.23 6.23-6.23 16.34 0 22.58L112.4 256 4.68 363.72c-6.23 6.23-6.23 16.34 0 22.58l25.03 25.03c6.23 6.23 16.34 6.23 22.58 0L160 303.6l107.72 107.72c6.23 6.23 16.34 6.23 22.58 0l25.03-25.03c6.23-6.23 6.23-16.34 0-22.58L207.6 256z"
                ></path>
                <!--v-if-->
              </svg></span
            ><span id="multiselectname" class="vfb-config-panel-header-label">{{
              targetElementData?.identification
            }}</span>
          </div>
          <div class="vfb-config-panel-header-wrapper-right">
            <!-- Clone -->
            <div
              class="vfb-config-panel-header-clone"
              tabindex="0"
              role="button"
              aria-label="Clone"
              @click="cloneImageElement"
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
                  d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zm-80 464c0 8.82-7.18 16-16 16H48c-8.82 0-16-7.18-16-16V144c0-8.82 7.18-16 16-16h48v240c0 26.51 21.49 48 48 48h240v48zm96-96c0 8.82-7.18 16-16 16H144c-8.82 0-16-7.18-16-16V48c0-8.82 7.18-16 16-16h320c8.82 0 16 7.18 16 16v320z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <!-- Remove -->
            <div
              class="vfb-config-panel-header-remove"
              tabindex="0"
              role="button"
              aria-label="Remove"
              @click="deleteElement"
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
                  d="M296 432h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zm-160 0h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zM440 64H336l-33.6-44.8A48 48 0 0 0 264 0h-80a48 48 0 0 0-38.4 19.2L112 64H8a8 8 0 0 0-8 8v16a8 8 0 0 0 8 8h24v368a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V96h24a8 8 0 0 0 8-8V72a8 8 0 0 0-8-8zM171.2 38.4A16.1 16.1 0 0 1 184 32h80a16.1 16.1 0 0 1 12.8 6.4L296 64H152zM384 464a16 16 0 0 1-16 16H80a16 16 0 0 1-16-16V96h320zm-168-32h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div
              class="vfb-config-panel-header-collapse vv-vfb-icon-plus"
              tabindex="0"
              role="button"
              aria-label="Expand all"
              @click="ColapsToggleExpand"
            >
              <svg
                class="vfb-icon vfb-config-panel-header-collapse-icon-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 206h-98v-98c0-6.6-5.4-12-12-12h-12c-6.6 0-12 5.4-12 12v98h-98c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h98v98c0 6.6 5.4 12 12 12h12c6.6 0 12-5.4 12-12v-98h98c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div
              class="vfb-config-panel-header-collapse d-none vv-vfb-icon-close"
              tabindex="0"
              role="button"
              aria-label="Collapse all"
              @click="ColapsToggleClose"
            >
              <svg
                class="vfb-icon vfb-config-panel-header-collapse-icon-close"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 242c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12H108c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h232z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Properties</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Name</span
                ><input
                  @change="setElementiImageAttribute($event, 'name')"
                  :value="targetElementData?.name"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input form-p-input-sm h-32"
                  value="multiImage"
                />
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Label</span
                ><textarea
                  @input="setElementiImageAttribute($event, 'label')"
                  :value="targetElementData?.label"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                  value="Multi-image"
                ></textarea>
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                  >Tooltip</span
                >
                <textarea
                  data-v-2a324127=""
                  type="text"
                  @input="setElementiImageAttribute($event, 'tooltip')"
                  :value="targetElementData?.tooltip"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                ></textarea>
              </div>
            </div>
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Description</span
                >
                <textarea
                  @input="setElementiImageAttribute($event, 'description')"
                  :value="targetElementData?.description"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                ></textarea>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Content</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center"
                  >Image url
                </span>
                <textarea
                  name="src"
                  id="options.img.src"
                  class="w-full bg-transparent h-full form-p-input-sm form-radius-large-sm form-text-sm with-floating:form-p-input-floating-sm form-color-input-success form-autofill-success"
                  placeholder="https://your-image-url"
                  rows="1"
                  aria-labelledby="options.img.src__label"
                  aria-describedby="options.img.src__description options.img.src__info"
                  aria-invalid="false"
                  @input="setElementiImageAttribute($event, 'imgurl')"
                  :value="targetElementData?.imgurl"
                  aria-errormessage="options.img.src__error"
                  aria-disabled="false"
                  aria-busy="false"
                  data-autogrow="true"
                  style="
                    overflow: hidden;
                    overflow-wrap: break-word;
                    resize: none;
                    text-align: start;
                    height: 52px;
                  "
                ></textarea>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 form-text-Inner text-black position-relative d-flex align-items-center"
                  >Alternate Text</span
                >
                <input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementiImageAttribute($event, 'alt')"
                  :value="targetElementData?.alt"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-start mt-2"
              >
                <span
                  class="fs-14 form-text-Inner text-black position-relative d-flex align-items-center form-bg-info"
                  >Title
                </span>
                <input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementiImageAttribute($event, 'inputtitle')"
                  :value="targetElementData?.inputtitle"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>

              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Width</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementiImageAttribute($event, 'width')"
                    :value="targetElementData?.width"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center vfb_form_info form-bg-info"
                  >Height</span
                >
                <div class="vfb_form_fonts d-flex justify-content-end position-relative">
                  <input
                    @input="setElementiImageAttribute($event, 'height')"
                    :value="targetElementData?.height"
                    class="form-control w-50 bg-input"
                    type="number"
                    id=""
                  />
                  <p class="mb-0 position-absolute vfb_fontPX">px</p>
                </div>
              </div>
            </div>

            <div class="vfb-faqs-body-inner">
              <div
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span
                  class="fs-14 form-text-Inner text-black position-relative d-flex align-items-center"
                  >Link url</span
                >
                <input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementiImageAttribute($event, 'linkurl')"
                  :value="targetElementData?.linkurl"
                  class="bg-input form-p-input-sm h-32"
                  placeholder="https://..."
                />
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-3"
              >
                <span
                  data-v-2a324127=""
                  class="fs-14 text-black position-relative d-flex align-items-center"
                  >Link Target
                </span>

                <select
                  class="form-p-input-sm bg-input w-full transition-input duration-200 border-solid form-border-width-input form-shadow-input form-py-input-sm form-pl-input-sm form-pr-select-no-clear-sm form-radius-input-sm form-text-sm form-min-h-input-height-inner-sm with-floating:form-p-input-floating-sm rtl:form-pr-input-sm rtl:form-pl-select-no-clear-sm form-bg-input-success form-color-input-success form-border-color-input-success hover:form-shadow-input-hover focused:form-shadow-input-focus focused:form-ring focused-hover:form-shadow-input-hover"
                  name="inputType"
                  id="properties.inputType"
                  aria-labelledby="properties.inputType__label"
                  aria-describedby="properties.inputType__description properties.inputType__info"
                  aria-invalid="false"
                  aria-errormessage="properties.inputType__error"
                  aria-disabled="false"
                  aria-busy="false"
                  @change="setElementiImageAttribute($event, 'target')"
                  :value="targetElementData?.target"
                >
                  <option value="_selft" selected>_selft</option>
                  <option value="_black">_black</option>
                  <option value="_parent">_parent</option>
                  <option value="_top">_top</option>
                </select>
              </div>
            </div>
            <div data-v-c98426aa="" class="vfb-faqs-body-inner" data-v-7ebfecff="">
              <div class="form-text-sm d-flex justify-content-between align-items-center">
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center"
                >
                  Custom attributes
                  <a href="#" class="vfb-learn-more ms-2" target="_blank">learn more</a>
                </span>
                <button
                  @click="addAttributes"
                  class="inline-block form-bg-primary border-0 form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                  role="button"
                  tabindex="0"
                >
                  + Add
                </button>
              </div>
              <div aria-labelledby="attributes.attrs__label">
                <div
                  v-for="(attribute, key) in targetElementCustomAttributesArr"
                  :key="attribute.name"
                  class="d-flex align-items-center border-bottom checkclosehover position-relative mt-3"
                >
                  <button
                    @click="removeElementCustomAttribute($event, key)"
                    class="close-svg-add-more-option border-0 p-0"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 320 512"
                      fill="currentColor"
                    >
                      <path
                        d="M193.94 256L296.5 153.44l21.15-21.15c3.12-3.12 3.12-8.19 0-11.31l-22.63-22.63c-3.12-3.12-8.19-3.12-11.31 0L160 222.06 36.29 98.34c-3.12-3.12-8.19-3.12-11.31 0L2.34 120.97c-3.12 3.12-3.12 8.19 0 11.31L126.06 256 2.34 379.71c-3.12 3.12-3.12 8.19 0 11.31l22.63 22.63c3.12 3.12 8.19 3.12 11.31 0L160 289.94 262.56 392.5l21.15 21.15c3.12 3.12 8.19 3.12 11.31 0l22.63-22.63c3.12-3.12 3.12-8.19 0-11.31L193.94 256z"
                      />
                    </svg>
                  </button>
                  <input
                    type="text"
                    placeholder="Name"
                    :v-model="attribute.name"
                    class="add-more-option border-0 bg-transparent h-32 w-100 px-2 py-1 labelInput"
                  />
                  <span class="px-2">
                    <svg
                      class="vfb-icon cursor-pointer"
                      aria-hidden="true"
                      focusable="false"
                      role="img"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 448 512"
                    >
                      <path
                        class=""
                        fill="currentColor"
                        d="M311.03 131.515l-7.071 7.07c-4.686 4.686-4.686 12.284 0 16.971L387.887 239H12c-6.627 0-12 5.373-12 12v10c0 6.627 5.373 12 12 12h375.887l-83.928 83.444c-4.686 4.686-4.686 12.284 0 16.971l7.071 7.07c4.686 4.686 12.284 4.686 16.97 0l116.485-116c4.686-4.686 4.686-12.284 0-16.971L328 131.515c-4.686-4.687-12.284-4.687-16.97 0z"
                      />
                    </svg>
                  </span>
                  <input
                    @input="makeElementCustomAttribute($event)"
                    type="text"
                    placeholder="Value"
                    :v-model="attribute.value"
                    class="add-more-option border-0 bg-transparent px-2 py-1 h-32 w-100 valueInput"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Decorators</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Before</span
                ><input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementiImageAttribute($event, 'before')"
                  :value="targetElementData?.before"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Between</span
                ><input
                  data-v-2a324127=""
                  type="text"
                  @input="setElementiImageAttribute($event, 'between')"
                  :value="targetElementData?.between"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>

              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span data-v-2a324127="" class="fs-14 text-black">After</span
                ><input
                  data-v-2a324127=""
                  @input="setElementiImageAttribute($event, 'after')"
                  :value="targetElementData?.after"
                  type="text"
                  class="bg-input form-p-input-sm h-32"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Layout</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div
              class="form-text-sm d-flex justify-content-between align-items-baseline vfb-faqs-body-inner border-bottom-0"
              data-v-2a324127=""
            >
              <span
                class="fs-14 text-black position-relative d-flex align-items-center"
                data-v-2a324127=""
                >Align
              </span>
              <div class="btn-group border" data-v-2a324127="">
                <button
                  @click="setElementAlignmentImage($event, 'alignment', 'text-start')"
                  type="button"
                  data-alignment="text-start"
                  class="btn fs-12 vf-primary text-white h-100 px-3"
                  :class="{
                    activeBtnClass: targetElementData?.alignment == 'text-start',
                  }"
                  data-v-2a324127=""
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
                      d="M12.83 352h262.34A12.82 12.82 0 0 0 288 339.17v-38.34A12.82 12.82 0 0 0 275.17 288H12.83A12.82 12.82 0 0 0 0 300.83v38.34A12.82 12.82 0 0 0 12.83 352zm0-256h262.34A12.82 12.82 0 0 0 288 83.17V44.83A12.82 12.82 0 0 0 275.17 32H12.83A12.82 12.82 0 0 0 0 44.83v38.34A12.82 12.82 0 0 0 12.83 96zM432 160H16a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h416a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16zm0 256H16a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h416a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16z"
                    ></path>
                    <!--v-if-->
                  </svg></button
                ><button
                  data-alignment="text-center"
                  @click="setElementAlignmentImage($event, 'alignment', 'text-center')"
                  :class="{
                    activeBtnClass: targetElementData?.alignment == 'text-center',
                  }"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
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
                      d="M432 160H16a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h416a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16zm0 256H16a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h416a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16zM108.1 96h231.81A12.09 12.09 0 0 0 352 83.9V44.09A12.09 12.09 0 0 0 339.91 32H108.1A12.09 12.09 0 0 0 96 44.09V83.9A12.1 12.1 0 0 0 108.1 96zm231.81 256A12.09 12.09 0 0 0 352 339.9v-39.81A12.09 12.09 0 0 0 339.91 288H108.1A12.09 12.09 0 0 0 96 300.09v39.81a12.1 12.1 0 0 0 12.1 12.1z"
                    ></path>
                    <!--v-if-->
                  </svg></button
                ><button
                  data-alignment="text-end"
                  @click="setElementAlignmentImage($event, 'alignment', 'text-end')"
                  :class="{ activeBtnClass: targetElementData?.alignment == 'text-end' }"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
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
                      d="M16 224h416a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16H16a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16zm416 192H16a16 16 0 0 0-16 16v32a16 16 0 0 0 16 16h416a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16zm3.17-384H172.83A12.82 12.82 0 0 0 160 44.83v38.34A12.82 12.82 0 0 0 172.83 96h262.34A12.82 12.82 0 0 0 448 83.17V44.83A12.82 12.82 0 0 0 435.17 32zm0 256H172.83A12.82 12.82 0 0 0 160 300.83v38.34A12.82 12.82 0 0 0 172.83 352h262.34A12.82 12.82 0 0 0 448 339.17v-38.34A12.82 12.82 0 0 0 435.17 288z"
                    ></path>
                    <!--v-if-->
                  </svg>
                </button>
              </div>
            </div>
            <div
              class="form-text-sm d-flex justify-content-between align-items-center vfb-faqs-body-inner"
              data-v-2a324127=""
            >
              <span
                class="fs-14 text-black position-relative d-flex align-items-baseline"
                data-v-2a324127=""
                >Space top
              </span>
              <div class="btn-group border" data-v-2a324127="">
                <button
                  @click="setElementSpaceTopImage($event, 'alignment', 'mt-0')"
                  :class="{ activeBtnClass: targetElementData?.spacetop == 'mt-0' }"
                  space-top="mt-1"
                  type="button"
                  class="btn fs-12 vf-primary text-white h-100 px-2"
                  data-v-2a324127=""
                >
                  None</button
                ><button
                  @click="setElementSpaceTopImage($event, 'spacetop', 'mt-1')"
                  :class="{ activeBtnClass: targetElementData?.spacetop == 'mt-1' }"
                  space-top="mt-1"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  1</button
                ><button
                  @click="setElementSpaceTopImage($event, 'spacetop', 'mt-2')"
                  :class="{ activeBtnClass: targetElementData?.spacetop == 'mt-2' }"
                  space-top="mt-2"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  2</button
                ><button
                  @click="setElementSpaceTopImage($event, 'spacetop', 'mt-3')"
                  :class="{ activeBtnClass: targetElementData?.spacetop == 'mt-3' }"
                  space-top="mt-3"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  3
                </button>
              </div>
            </div>
            <div
              class="form-text-sm d-flex justify-content-between align-items-center vfb-faqs-body-inner border-bottom-0"
              data-v-2a324127=""
            >
              <span
                class="fs-14 text-black position-relative d-flex align-items-baseline"
                data-v-2a324127=""
                >Space bottom
              </span>
              <div class="btn-group border" data-v-2a324127="">
                <button
                  @click="setElementSpaceBottomImage($event, 'spacebottom', 'mb-0')"
                  :class="{ activeBtnClass: targetElementData?.spacebottom == 'mb-0' }"
                  space-bottom="mb-0"
                  type="button"
                  class="btn fs-12 vf-primary text-white h-100 px-2"
                  data-v-2a324127=""
                >
                  None</button
                ><button
                  @click="setElementSpaceBottomImage($event, 'spacebottom', 'mb-1')"
                  :class="{ activeBtnClass: targetElementData?.spacebottom == 'mb-1' }"
                  space-bottom="mb-1"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  1</button
                ><button
                  @click="setElementSpaceBottomImage($event, 'spacebottom', 'mb-2')"
                  :class="{ activeBtnClass: targetElementData?.spacebottom == 'mb-2' }"
                  space-bottom="mb-2"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  2</button
                ><button
                  @click="setElementSpaceBottomImage($event, 'spacebottom', 'mb-3')"
                  :class="{ activeBtnClass: targetElementData?.spacebottom == 'mb-3' }"
                  space-bottom="mb-3"
                  type="button"
                  class="btn fs-12 border-start bg-light px-3"
                  data-v-2a324127=""
                >
                  3
                </button>
              </div>
            </div>

            <div
              class="form-text-sm d-flex justify-content-between align-items-center vfb-faqs-body-inner border-bottom-0"
            >
              <span class="fs-14 text-black position-relative d-flex align-items-center"
                >Size
                <a href="##" class="vfb-learn-more ms-2" target="_blank"
                  >learn more</a
                ></span
              >
              <div class="btn-group border">
                <button
                  @click="setElementSizeAttribute($event, 'size', 'font-default')"
                  type="button"
                  class="btn fs-12 h-100 px-2 activeBtnClass"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-default',
                  }"
                >
                  Default</button
                ><button
                  @click="setElementSizeAttribute($event, 'size', 'font-sm')"
                  type="button"
                  class="btn fs-12 border-start px-3"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-sm',
                  }"
                >
                  sm</button
                ><button
                  @click="setElementSizeAttribute($event, 'size', 'font-md')"
                  type="button"
                  class="btn fs-12 border-start px-3"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-md',
                  }"
                >
                  md</button
                ><button
                  @click="setElementSizeAttribute($event, 'size', 'font-lg')"
                  type="button"
                  class="btn fs-12 border-start px-3"
                  :class="{
                    activeBtnClass: targetElementData?.size == 'font-lg',
                  }"
                >
                  lg
                </button>
              </div>
            </div>

            <section class="singleimage-layout">
              <div
                class="form-text-sm d-flex flex-wrap justify-content-between align-items-center mt-2 vfb-faqs-body-inner border-bottom-0"
              >
                <span
                  class="fs-14 text-black position-relative d-flex align-items-center form-bg-info"
                >
                  Columns
                  <a href="#" class="vfb-learn-more ms-2" target="_blank">learn more</a>
                </span>
                <div class="w-100 py-2">
                  <ul
                    class="nav nav-pills border category_tabs container_tabs"
                    id="singleimage-tab"
                    role="tablist"
                  >
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link active text-black tabFirst w-100"
                        id="singleimage-default-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#singleimage-default"
                        type="button"
                        role="tab"
                        aria-controls="select-default"
                        aria-selected="true"
                      >
                        Default
                      </button>
                    </li>
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link text-black tabCenter w-100"
                        id="singleimage-tablet-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#singleimage-tablet"
                        type="button"
                        role="tab"
                        aria-controls="select-tablet"
                        aria-selected="false"
                      >
                        Tablet
                      </button>
                    </li>
                    <li class="nav-item" role="presentation">
                      <button
                        class="nav-link text-black tablast w-100"
                        id="singleimage-desktop-tab"
                        data-bs-toggle="pill"
                        data-bs-target="#singleimage-desktop"
                        type="button"
                        role="tab"
                        aria-controls="select-desktop"
                        aria-selected="false"
                      >
                        Desktop
                      </button>
                    </li>
                  </ul>

                  <div class="tab-content">
                    <!-- Default Tab -->
                    <div
                      class="tab-pane fade show active"
                      id="singleimage-default"
                      role="tabpanel"
                      aria-labelledby="input-default-tab"
                    >
                      <!-- Content for Default Tab -->
                      <section>
                        <div
                          class="w-100 d-flex justify-content-between align-items-items-center py-3"
                        >
                          <div class="fs-14 text-64748B">DEFAULT</div>
                          <div class="text-xs fs-14 text-64748B">
                            Viewport size &gt;=0px
                          </div>
                        </div>

                        <div class="w-100 py-3 tab-inner-content">
                          <ul
                            class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                            id="cont-tab"
                            role="tablist"
                          >
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link active text-black tabFirst w-100"
                                id="singleimage-container-tab"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-container"
                                type="button"
                                role="tab"
                                aria-controls="pills-cont"
                                aria-selected="true"
                              >
                                Container
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tabCenter w-100"
                                id="singleimage-label-tab"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-label"
                                type="button"
                                role="tab"
                                aria-controls="pills-lebal"
                                aria-selected="false"
                              >
                                Label
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tablast w-100"
                                id="singleimage-wrapper-tab"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-wrapper"
                                type="button"
                                role="tab"
                                aria-controls="pills-Wrapper"
                                aria-selected="false"
                              >
                                Wrapper
                              </button>
                            </li>
                          </ul>

                          <div class="tab-content" id="default-tabContent">
                            <div
                              class="tab-pane fade show active"
                              id="singleimage-container"
                              role="tabpanel"
                              aria-labelledby="input-container-tab"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Container width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.default.container ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.container ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.container ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'default',
                                          'container',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="singleimage-label"
                              role="tabpanel"
                              aria-labelledby="input-label-tab"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Label width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.default.label ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.label ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.label ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'default',
                                          'label',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="singleimage-wrapper"
                              role="tabpanel"
                              aria-labelledby="input-wrapper-tab"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Wrapper width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.default.wrapper ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.wrapper ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.default.wrapper ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'default',
                                          'wrapper',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </section>
                      <!-- Content for Default Tab -->
                    </div>

                    <!-- Tablet Tab -->
                    <div
                      class="tab-pane fade"
                      id="singleimage-tablet"
                      role="tabpanel"
                      aria-labelledby="input-tablet-tab"
                    >
                      <!-- Content for Tablet Tab -->
                      <section>
                        <div
                          class="w-100 d-flex justify-content-between align-items-items-center py-3"
                        >
                          <div class="fs-14 text-64748B">TABLET</div>
                          <div class="text-xs fs-14 text-64748B">
                            Viewport size &gt;=640px
                          </div>
                        </div>

                        <div class="w-100 py-3 tab-inner-content">
                          <ul
                            class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                            id="cont-tab1"
                            role="tablist"
                          >
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link active text-black tabFirst w-100"
                                id="singleimage-container-tab1"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-container1"
                                type="button"
                                role="tab"
                                aria-controls="pills-cont"
                                aria-selected="true"
                              >
                                Container
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tabCenter w-100"
                                id="singleimage-label-tab1"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-label1"
                                type="button"
                                role="tab"
                                aria-controls="pills-lebal"
                                aria-selected="false"
                              >
                                Label
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tablast w-100"
                                id="singleimage-wrapper-tab1"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-wrapper1"
                                type="button"
                                role="tab"
                                aria-controls="pills-Wrapper"
                                aria-selected="false"
                              >
                                Wrapper
                              </button>
                            </li>
                          </ul>

                          <div class="tab-content" id="default-tabContent1">
                            <div
                              class="tab-pane fade show active"
                              id="singleimage-container1"
                              role="tabpanel"
                              aria-labelledby="input-container-tab1"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Container width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'container',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="singleimage-label1"
                              role="tabpanel"
                              aria-labelledby="input-label-tab1"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Label width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.tablet.label ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.label ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.label ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'tablet',
                                          'label',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="singleimage-wrapper1"
                              role="tabpanel"
                              aria-labelledby="input-wrapper-tab1"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Wrapper width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.tablet.wrapper ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.wrapper ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.tablet.wrapper ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'tablet',
                                          'wrapper',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </section>
                      <!-- Content for Tablet Tab -->
                    </div>

                    <!-- Desktop Tab -->
                    <div
                      class="tab-pane fade"
                      id="singleimage-desktop"
                      role="tabpanel"
                      aria-labelledby="input-desktop-tab"
                    >
                      <!-- Content for Desktop Tab -->
                      <section>
                        <div
                          class="w-100 d-flex justify-content-between align-items-items-center py-3"
                        >
                          <div class="fs-14 text-64748B">DESKTOP</div>
                          <div class="text-xs fs-14 text-64748B">
                            Viewport size &gt;=1024px
                          </div>
                        </div>

                        <div class="w-100 py-3 tab-inner-content">
                          <ul
                            class="nav nav-pills border mb-3 category_tabs container_tabs default_tabs"
                            id="cont-tab2"
                            role="tablist"
                          >
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link active text-black tabFirst w-100"
                                id="singleimage-container-tab2"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-container2"
                                type="button"
                                role="tab"
                                aria-controls="pills-cont"
                                aria-selected="true"
                              >
                                Container
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tabCenter w-100"
                                id="singleimage-label-tab2"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-label2"
                                type="button"
                                role="tab"
                                aria-controls="pills-lebal"
                                aria-selected="false"
                              >
                                Label
                              </button>
                            </li>
                            <li class="nav-item" role="presentation">
                              <button
                                class="nav-link text-black tablast w-100"
                                id="singleimage-wrapper-tab2"
                                data-bs-toggle="pill"
                                data-bs-target="#singleimage-wrapper2"
                                type="button"
                                role="tab"
                                aria-controls="pills-Wrapper"
                                aria-selected="false"
                              >
                                Wrapper
                              </button>
                            </li>
                          </ul>

                          <div class="tab-content" id="default-tabContent2">
                            <div
                              class="tab-pane fade show active"
                              id="singleimage-container2"
                              role="tabpanel"
                              aria-labelledby="input-container-tab2"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Container width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.container ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'container',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="singleimage-label2"
                              role="tabpanel"
                              aria-labelledby="input-label-tab2"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Label width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.label ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.label ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.label ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'label',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>

                            <div
                              class="tab-pane fade"
                              id="singleimage-wrapper2"
                              role="tabpanel"
                              aria-labelledby="input-wrapper-tab2"
                            >
                              <div class="w-100">
                                <div class="mt-3">
                                  <div
                                    class="w-100 d-flex justify-content-between align-items-items-center"
                                  >
                                    <div class="fs-14 text-64748B">Wrapper width:</div>
                                    <div class="text-xs fs-14 text-64748B">1/12</div>
                                  </div>
                                  <div class="btn-group border w-100 mt-3">
                                    <button
                                      v-for="column in 12"
                                      :key="column"
                                      type="button"
                                      class="btn fs-12 bg-light h-100 px-1"
                                      :class="{
                                        activeBtnClass:
                                          targetElementColumns.desktop.wrapper ===
                                          `col-lg-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.wrapper ===
                                          `col-md-${column}`,
                                        activeBtnClass:
                                          targetElementColumns.desktop.wrapper ===
                                          `col-sm-${column}`,
                                      }"
                                      @click="
                                        setElementColumns(
                                          $event,
                                          'desktop',
                                          'wrapper',
                                          column
                                        )
                                      "
                                    >
                                      {{ column }}
                                    </button>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </section>
                      <!-- Content for Desktop Tab -->
                    </div>
                  </div>
                </div>
              </div>
            </section>
          </div>
        </div>
      </div>

      <div class="vfb-faqs d-none">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Conditions</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm vfb_element_section d-flex justify-content-between align-items-center"
              >
                <span data-v-2a324127="" class="fs-14 text-black"
                  >The element has no conditions</span
                >
                <!-- Button trigger modal -->
                <button
                  @click="showModel($event)"
                  type="button"
                  class="btn text-white vfb_model_condition"
                  data-bs-toggle="modal"
                  data-bs-target="#exampleModal"
                >
                  Edit
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!--  Tab ------------------------------ Tab -->
  <div class="vfb-right-container" style="right: -500px" id="rightMenuTab">
    <div class="position-relative h-100"></div>
    <div class="vfb-panels-wrapper-multiselect">
      <div class="vfb-config-panel-header-container">
        <div class="vfb-config-panel-header">
          <div class="vfb-config-panel-header-wrapper-left">
            <span
              class="vfb-config-panel-header-close"
              tabindex="0"
              @click="TabsClose"
              role="button"
              aria-label="Close config panel"
              ><svg
                class="vfb-icon vfb-config-panel-header-close-icon"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 320 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M207.6 256l107.72-107.72c6.23-6.23 6.23-16.34 0-22.58l-25.03-25.03c-6.23-6.23-16.34-6.23-22.58 0L160 208.4 52.28 100.68c-6.23-6.23-16.34-6.23-22.58 0L4.68 125.7c-6.23 6.23-6.23 16.34 0 22.58L112.4 256 4.68 363.72c-6.23 6.23-6.23 16.34 0 22.58l25.03 25.03c6.23 6.23 16.34 6.23 22.58 0L160 303.6l107.72 107.72c6.23 6.23 16.34 6.23 22.58 0l25.03-25.03c6.23-6.23 6.23-16.34 0-22.58L207.6 256z"
                ></path>
                <!--v-if-->
              </svg></span
            ><span id="multiselectname" class="vfb-config-panel-header-label">{{
              targetTabData?.name
            }}</span>
          </div>
          <div class="vfb-config-panel-header-wrapper-right">
            <!-- Clone -->
            <div
              class="vfb-config-panel-header-clone"
              tabindex="0"
              role="button"
              aria-label="Clone"
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
                  d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zm-80 464c0 8.82-7.18 16-16 16H48c-8.82 0-16-7.18-16-16V144c0-8.82 7.18-16 16-16h48v240c0 26.51 21.49 48 48 48h240v48zm96-96c0 8.82-7.18 16-16 16H144c-8.82 0-16-7.18-16-16V48c0-8.82 7.18-16 16-16h320c8.82 0 16 7.18 16 16v320z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <!-- Remove -->
            <div
              class="vfb-config-panel-header-remove"
              tabindex="0"
              role="button"
              aria-label="Remove"
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
                  d="M296 432h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zm-160 0h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8zM440 64H336l-33.6-44.8A48 48 0 0 0 264 0h-80a48 48 0 0 0-38.4 19.2L112 64H8a8 8 0 0 0-8 8v16a8 8 0 0 0 8 8h24v368a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V96h24a8 8 0 0 0 8-8V72a8 8 0 0 0-8-8zM171.2 38.4A16.1 16.1 0 0 1 184 32h80a16.1 16.1 0 0 1 12.8 6.4L296 64H152zM384 464a16 16 0 0 1-16 16H80a16 16 0 0 1-16-16V96h320zm-168-32h16a8 8 0 0 0 8-8V152a8 8 0 0 0-8-8h-16a8 8 0 0 0-8 8v272a8 8 0 0 0 8 8z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div
              class="vfb-config-panel-header-collapse vv-vfb-icon-plus"
              tabindex="0"
              role="button"
              aria-label="Expand all"
              @click="ColapsToggleExpand"
            >
              <svg
                class="vfb-icon vfb-config-panel-header-collapse-icon-open"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                handle
                <path
                  class=""
                  fill="currentColor"
                  d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 206h-98v-98c0-6.6-5.4-12-12-12h-12c-6.6 0-12 5.4-12 12v98h-98c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h98v98c0 6.6 5.4 12 12 12h12c6.6 0 12-5.4 12-12v-98h98c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
            <div
              class="vfb-config-panel-header-collapse d-none vv-vfb-icon-close"
              tabindex="0"
              role="button"
              aria-label="Collapse all"
              @click="ColapsToggleClose"
            >
              <svg
                class="vfb-icon vfb-config-panel-header-collapse-icon-close"
                aria-hidden="true"
                focusable="false"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                <path
                  class=""
                  fill="currentColor"
                  d="M400 64c8.8 0 16 7.2 16 16v352c0 8.8-7.2 16-16 16H48c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h352m0-32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zm-60 242c6.6 0 12-5.4 12-12v-12c0-6.6-5.4-12-12-12H108c-6.6 0-12 5.4-12 12v12c0 6.6 5.4 12 12 12h232z"
                ></path>
                <!--v-if-->
              </svg>
            </div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Properties</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div
                data-v-2a324127=""
                class="form-text-sm d-flex justify-content-between align-items-center mt-2"
              >
                <span data-v-2a324127="" class="fs-14 text-black">Name</span
                ><textarea
                  @input="setTabName($event)"
                  :value="targetTabData?.name"
                  data-v-2a324127=""
                  type="text"
                  class="bg-input vfb_multiimg_textarea form-p-input-sm h-32"
                  value="Multi-image"
                ></textarea>
              </div>
            </div>
            <div class="vfb-faqs-body-inner"></div>
          </div>
        </div>
      </div>
      <div class="vfb-faqs">
        <div class="vfb-faqs-item">
          <div
            @click="handleClick"
            class="vfb-faqs-item-inner cursor-pointer d-flex justify-content-between align-items-center"
          >
            <span class="medium text-black">Conditions</span>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-open"
              aria-hidden="true"
              focusable="false"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                fill="#94a3b8"
                d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
            <svg
              width="12px"
              height="12px"
              class="vfb-icon vfb-config-form-header-collapse-close d-none"
              aria-hidden="true"
              focusable="false"
              fill="#94a3b8"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
            >
              <path
                class=""
                d="M368 224H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h352c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"
              ></path>
              <!--v-if-->
            </svg>
          </div>
          <div class="vfb-faqs-body bg-white" style="display: none">
            <div class="vfb-faqs-body-inner">
              <div class="form-text-sm d-flex justify-content-between align-items-center">
                <span class="fs-14 text-black">The element has no conditions</span>
                <div
                  @click="showModel($event)"
                  class="inline-block form-bg-primary form-border-width-btn form-border-color-primary form-color-on-primary form-shadow-btn ease-linear transition-transform transform hover:scale-105 focus:form-ring vfb-util-props-list-add form-mt-gutter-sm form-radius-small-sm form-text-small-sm form-p-btn-small-sm"
                  id="validation.validation_wrapper.rules-add-button"
                  role="button"
                  tabindex="0"
                >
                  + Edit
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div
    class="vfb-model-preview-container-right-array p-3"
    style="right: -500px"
    id="vfbmodelarray"
  >
    <div class="d-flex justify-content-between">
      <h6 class="text-white vfb-model">Data</h6>
      <div class="vfb-model-preview-close" tabindex="0">
        <svg
          @click="vfbmodelarrayClose()"
          class="vfb-icon vfb-model-preview-close-icon"
          aria-hidden="true"
          focusable="false"
          role="img"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 320 512"
        >
          <path
            class=""
            fill="#94a3b8"
            d="M207.6 256l107.72-107.72c6.23-6.23 6.23-16.34 0-22.58l-25.03-25.03c-6.23-6.23-16.34-6.23-22.58 0L160 208.4 52.28 100.68c-6.23-6.23-16.34-6.23-22.58 0L4.68 125.7c-6.23 6.23-6.23 16.34 0 22.58L112.4 256 4.68 363.72c-6.23 6.23-6.23 16.34 0 22.58l25.03 25.03c6.23 6.23 16.34 6.23 22.58 0L160 303.6l107.72 107.72c6.23 6.23 16.34 6.23 22.58 0l25.03-25.03c6.23-6.23 6.23-16.34 0-22.58L207.6 256z"
          ></path>
          <!--v-if-->
        </svg>
      </div>
    </div>
    <div class="text-white" ref="finalArrParentElement">
      <pre>{{ JSON.stringify(finalArr, null, 2) }}</pre>
    </div>
  </div>
  <!-- < MULTISELECT  ------------------------------ > MULTISELECT -->

  <!-- <  ------------------------------ > -->
  <!-- <  MODAL ------------------------------ MODAL > -->
  <!-- <  MODAL ------------------------------ MODAL > -->
  <div
    class="modal"
    id="exampleModal"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    style=""
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content shadow">
        <div
          class="modal-header vfb_condition_popup d-flex align-items-center px-4 py-3 vfb_model_reset"
        >
          <div>
            <h3 class="modal-title" id="exampleModalLabel">Conditions</h3>
            <p class="mb-0">Multi-image</p>
          </div>
          <button
            type="button"
            @click="closeModel($event)"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <div class="p-0">
            <div class="d-none p-3">
              <div class="vfb-condition-list">
                <div
                  v-for="(item, index) in items"
                  :key="index"
                  :data-id="'main-condition-' + index"
                  class="vfb-condition-main-section mb-3"
                >
                  <div class="vfb-condition-inner-section">
                    <div class="row">
                      <div class="col-lg-3">
                        <div class="position-relative vfb-condition-main">
                          <span> </span>
                          <select
                            class="form-control p-2"
                            name="text"
                            :id="
                              'conditions.' +
                              index +
                              '.conditions.' +
                              index +
                              '.field__info'
                            "
                            placeholder="Field"
                          >
                            <option value="" disabled selected>Select Field</option>
                            <option
                              v-for="(element, index) in getListOfElements"
                              :key="index"
                            >
                              {{ element.identification }}
                            </option>
                          </select>
                          <div class="position-absolute vfb-condition-input-list">
                            <svg
                              xmlns="http://www.w3.org/2000/svg"
                              width="13"
                              height="13"
                              fill="#63738a"
                              class="bi bi-caret-down-fill"
                              viewBox="0 0 16 16"
                            >
                              <path
                                d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                              />
                            </svg>
                          </div>
                          <div
                            @click="removeHtmlMain($event, index)"
                            class="vfb-condition-hover"
                          >
                            <svg
                              xmlns="http://www.w3.org/2000/svg"
                              width="10"
                              height="10"
                              fill="currentColor"
                              class="bi bi-x-lg"
                              viewBox="0 0 16 16"
                            >
                              <path
                                d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"
                              />
                            </svg>
                          </div>
                        </div>
                      </div>
                      <div class="col-lg-9 check_conditions">
                        <div class="position-relative">
                          <select
                            @change="checkCondition($event)"
                            class="form-control p-2"
                            name="text"
                            :id="
                              'conditions.' +
                              index +
                              '.conditions.' +
                              index +
                              '.expected__info'
                            "
                            placeholder="Field"
                          >
                            <option
                              value="is_empty"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              is empty
                            </option>
                            <option
                              value="is_not_empty"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              is not empty
                            </option>
                            <option
                              value="is_equal_to"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              is equal to
                            </option>
                            <option
                              value="is__not_equal_to"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              is not equal to
                            </option>
                            <option
                              value="is_greater"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              less then
                            </option>
                            <option
                              value="is_less"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              greater then
                            </option>
                            <option
                              value="starts_with"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              Starts With
                            </option>
                            <option
                              value="end_with"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              End with
                            </option>
                            <option
                              value="contains"
                              class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                            >
                              Contains
                            </option>
                          </select>
                          <div class="position-absolute vfb-condition-input-list">
                            <svg
                              xmlns="http://www.w3.org/2000/svg"
                              width="13"
                              height="13"
                              fill="#63738a"
                              class="bi bi-caret-down-fill"
                              viewBox="0 0 16 16"
                            >
                              <path
                                d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                              />
                            </svg>
                          </div>
                        </div>
                      </div>
                      <div class="col-lg-6 d-none check_conditions_input">
                        <input type="text" class="border rounded px-2 py-2 w-100" />
                      </div>
                    </div>
                    <div
                      v-for="subIndex in item.htmlinnerCount"
                      :key="subIndex"
                      :data-id="'sub-condition-' + index + '-' + subIndex"
                      class="vfb_condition_wrapper"
                    >
                      <div
                        class="vfb-condition-wrapper-list vfb-condition-wrapper-main mt-3"
                      >
                        <div class="row">
                          <div class="col-lg-3">
                            <div class="position-relative vfb-condition-main">
                              <select
                                :id="
                                  'subconditions.' +
                                  subIndex +
                                  '.conditions.' +
                                  subIndex +
                                  '.field__info'
                                "
                                class="form-control p-2"
                                name="text"
                                placeholder="Field"
                              >
                                <option value="" disabled selected>Select Field</option>
                                <option
                                  v-for="(element, index) in getListOfElements"
                                  :key="index"
                                >
                                  {{ element.identification }}
                                </option>
                              </select>
                              <div class="position-absolute vfb-condition-input-list">
                                <svg
                                  xmlns="http://www.w3.org/2000/svg"
                                  width="13"
                                  height="13"
                                  fill="#63738a"
                                  class="bi bi-caret-down-fill"
                                  viewBox="0 0 16 16"
                                >
                                  <path
                                    d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                                  />
                                </svg>
                              </div>
                              <div class="vfb-condition-hover">
                                <svg
                                  @click="removeHtmlInner(index, subIndex)"
                                  xmlns="http://www.w3.org/2000/svg"
                                  width="10"
                                  height="10"
                                  fill="currentColor"
                                  class="bi bi-x-lg"
                                  viewBox="0 0 16 16"
                                >
                                  <path
                                    d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"
                                  />
                                </svg>
                              </div>
                            </div>
                          </div>
                          <div class="col-lg-9 check_conditions">
                            <div class="position-relative">
                              <select
                                @change="checkCondition($event)"
                                class="form-control p-2"
                                name="text"
                                :id="
                                  'subconditions.' +
                                  subIndex +
                                  '.conditions.' +
                                  subIndex +
                                  '. '
                                "
                                placeholder="Field"
                              >
                                <option
                                  value="is_empty"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  is empty
                                </option>
                                <option
                                  value="is_not_empty"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  is not empty
                                </option>
                                <option
                                  value="is_equal_to"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  is equal to
                                </option>
                                <option
                                  value="is__not_equal_to"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  is not equal to
                                </option>
                                <option
                                  value="is_greater"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  less then
                                </option>
                                <option
                                  value="is_less"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  greater then
                                </option>
                                <option
                                  value="starts_with"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  Starts With
                                </option>
                                <option
                                  value="end_with"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  End with
                                </option>
                                <option
                                  value="contains"
                                  class="class=&quot;py-2 ps-3 vfb-field-text-primary&quot;"
                                >
                                  Contains
                                </option>
                              </select>
                              <div class="position-absolute vfb-condition-input-list">
                                <svg
                                  xmlns="http://www.w3.org/2000/svg"
                                  width="13"
                                  height="13"
                                  fill="#63738a"
                                  class="bi bi-caret-down-fill"
                                  viewBox="0 0 16 16"
                                >
                                  <path
                                    d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                                  />
                                </svg>
                              </div>
                            </div>
                          </div>
                          <div class="col-lg-6 d-none check_conditions_input">
                            <div class="">
                              <input type="text" class="border rounded px-2 py-2 w-100" />
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                    <div class="mt-3">
                      <button
                        @click="addHtmlInner(index)"
                        type="button"
                        class="btn text-white vfb_model_condition fs-14"
                      >
                        + OR
                      </button>
                    </div>
                  </div>
                </div>
              </div>
              <div class="mt-2">
                <button
                  @click="addMore1"
                  type="button"
                  class="btn text-white vfb_model_condition fs-14"
                >
                  + AND
                </button>
              </div>
            </div>

            <div class="vfb-conditions-empty-wrapper py-5">
              <div class="vfb-conditions-empty-icon">
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
                    d="M448 64v384a32 32 0 0 1-32 32H304a16 16 0 0 1-16-16v-32a16 16 0 0 1 16-16h80V96h-80a16 16 0 0 1-16-16V48a16 16 0 0 1 16-16h112a32 32 0 0 1 32 32z"
                  ></path>
                  <path
                    class="opacity-60"
                    fill="currentColor"
                    d="M144 32H32A32 32 0 0 0 0 64v384a32 32 0 0 0 32 32h112a16 16 0 0 0 16-16v-32a16 16 0 0 0-16-16H64V96h80a16 16 0 0 0 16-16V48a16 16 0 0 0-16-16z"
                  ></path>
                </svg>
              </div>
              <div class="vfb-conditions-empty-title">No conditions</div>
              <div class="vfb-conditions-empty-subtitle">The condition list is empty</div>
              <button
                @click="addCondition($event)"
                type="button"
                class="btn text-white vfb_model_condition mt-2"
              >
                Add Condition
              </button>
            </div>
            <div
              class="modal-footer d-flex justify-content-between align-items-center pb-0"
            >
              <div>
                <button type="button" class="btn text-white vfb_model_condition">
                  Save
                </button>
                <button type="button" class="btn text-black vfb_model_reset ms-2">
                  Reset
                </button>
              </div>
              <div>
                <button class="btn fs-16 text-black" href="#" @click="closeModel($event)">
                  Cancel
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- <  MODAL ------------------------------ MODAL > -->
  <!-- <  MODAL ------------------------------ MODAL > -->

  <!-- <  MODAL ------------------------------ MODAL > -->
</template>

<script>
// import Textfieldright from '../../components/Textfieldright.vue';
import { ref } from "vue";
import sidebar from './sidebar.vue'
import '../assets/css/global.css'
import '../assets/css/sidebar.css'
export default {

  name: "PreviewComponentBkp",
  data() {
    return {
      // rules: [],
      tabs: [],
      tabsCount: 0,
      items: [],
      options: [
        // Add default options here or load dynamically
        { id: 1, name: "Option 1", value: "Value 1" },
      ],
      uniqueSelectedItems: [],
      searchTerm: "",
      showDefaultUl: false,
      selectedItems: [],
      tab: false,
      targetTabKey: "",
      targetTabData: {},
      finalArr: {},
      currentTabID: "",
      acceptedTypes: [],
      targetElementConditions: [],
      tags: [],
      tagInput: "",
      tagOptions: [
        "application/epub+zip",
        "application/gzip",
        "application/java-archive",
        "application/json",
        "application/ld+json",
        "application/msword",
        "application/octet-stream",
        "application/ogg",
        "application/pdf",
        "application/rtf",
        "application/vnd.amazon.ebook",
        "application/vnd.apple.installer+xml",
        "application/vnd.mozilla.xul+xml",
        "application/vnd.ms-excel",
        "application/vnd.ms-fontobject",
        "application/vnd.ms-powerpoint",
        "application/vnd.oasis.opendocument.presentation",
        "application/vnd.oasis.opendocument.spreadsheet",
        "application/vnd.oasis.opendocument.text",
        "application/vnd.openxmlformats-officedocument.presentationml.presentation",
        "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
        "application/vnd.rar",
        "application/vnd.visio",
        "application/x-7z-compressed",
        "application/x-abiword",
        "application/x-bzip",
        "application/x-bzip2",
        "application/x-cdf",
        "application/x-csh",
        "application/x-freearc",
        "application/x-httpd-php",
        "application/x-sh",
        "application/x-shockwave-flash",
        "application/x-tar",
        "application/xhtml+xml",
        "application/xml",
        "application/zip",
        "audio/3gpp",
        "audio/3gpp2",
        "audio/aac",
        "audio/midi audio/x-midi",
        "audio/mpeg",
        "audio/ogg",
        "audio/opus",
        "audio/wav",
        "audio/webm",
        "font/otf",
        "font/ttf",
        "font/woff",
        "font/woff2",
        "image/avif",
        "image/gif",
        "image/heic",
        "image/jpeg",
        "image/png",
        "image/svg+xml",
        "image/tiff",
        "image/vnd.microsoft.icon",
        "image/webp",
        "text/calendar",
        "text/css",
        "text/csv",
        "text/html",
        "text/javascript",
        "text/plain",
        "video/3gpp",
        "video/3gpp2",
        "video/mp2t",
        "video/mp4",
        "video/mpeg",
        "video/ogg",
        "video/webm",
        "video/x-msvideo",
      ],
      tags2: [],
      tagInput2: "",
      tagOptions2: [
        "aac",
        "abw",
        "arc",
        "avif",
        "avi",
        "azw",
        "bin",
        "bmp",
        "bz",
        "bz2",
        "cda",
        "csh",
        "css",
        "csv",
        "doc",
        "docx",
        "eot",
        "epub",
        "gz",
        "gif",
        "heic",
        "heif",
        "htm",
        "html",
        "ico",
        "ics",
        "jar",
        "jpeg",
        "js",
        "json",
        "jsonld",
        "mid",
        "midi",
        "mjs",
        "mp3",
        "mp4",
        "mpeg",
        "mpkg",
        "odp",
        "ods",
        "odt",
        "oga",
        "ogv",
        "ogx",
        "opus",
        "otf",
        "png",
        "pdf",
        "php",
        "ppt",
        "pptx",
        "rar",
        "rtf",
        "sh",
        "svg",
        "swf",
        "tar",
        "tif",
        "tiff",
        "ts",
        "ttf",
        "txt",
        "vsd",
        "wav",
        "weba",
        "webm",
        "webp",
        "woff",
        "woff2",
        "xhtml",
        "xls",
        "xlsx",
        "xml",
        "xul",
        "zip",
        "3gp",
        "3g2",
        "7z",
      ],
      options2: [{ name: "Please Select", value: "" }],
      targetElementColumns: {
        default: {
          container: "col-lg-12",
          label: "col-lg-12",
          wrapper: "col-lg-12",
        },

        tablet: {
          container: "col-md-12 col-sm-12",
          label: "col-md-12 col-sm-12",
          wrapper: "col-md-12 col-sm-12",
        },
        desktop: {
          container: "col-lg-12",
          label: "col-lg-12",
          wrapper: "col-lg-12",
        },
      },
      targetElement: null,
      targetElementParent: null,
      targetElementData: {},
      targetElementCustomAttributes: [],
      elementCount: 0,
      multiSelectCount: 0,
      multiImageCount: 0,
      imageCount: 0,
      attributes: [],
      items_AO: [{ type: "", field: "" }], // Initial rule
      resultArrays: [],
      uploadedImageUrls:[],
      imageUrl:'',
    };
  },
  mounted() {
    // Add event listeners to relevant elements
    const draggableElements = document.querySelectorAll('[draggable="true"]');

    draggableElements.forEach((element) => {
      element.addEventListener("dragstart", this.handleDragStart);
      element.addEventListener("dragover", this.handleDragOver);
      element.addEventListener("drop", this.handleDrop);
    });

    const dropContainer = document.getElementById("drop-container");
    dropContainer.addEventListener("dragover", this.handleDragOver);
    dropContainer.addEventListener("drop", this.handleDrop);
  },
  update() {
    // Add event listeners to relevant elements
    const draggableElements = document.querySelectorAll('[draggable="true"]');

    draggableElements.forEach((element) => {
      element.addEventListener("dragstart", this.handleDragStart);
      element.addEventListener("dragover", this.handleDragOver);
      element.addEventListener("drop", this.handleDrop);
    });
  },
  watch: {
    finalArr(newVal, oldVal) {
      this.$refs.finalArrParentElement.innerHTML = `<pre>${JSON.stringify(
        newVal,
        null,
        2
      )}</pre>`;
      return newVal;
    },
  },
  computed: {
    targetElementCustomAttributesArr() {
      return this.targetElementData.customAttributes
        ? this.targetElementData.customAttributes.slice()
        : [];
    },
    getListOfElements() {
      let targetKey = this.targetTabKey;
      return this.tab == true
        ? this.finalArr[targetKey] && this.finalArr[targetKey].elements != undefined
          ? this.finalArr[targetKey].elements
          : []
        : this.finalArr;
    },
  },
  methods: {
    addItem() {
      this.items_AO.push({ type: "", field: "" });
    },
    removeItem(index, targetAttribute) {
      this.items_AO.splice(index, 1);
      this.resultArrays.splice(index, 1);
      this.setOrUpdateTargetElementData(targetAttribute, this.resultArrays.flat());
    },
    handleTypeChange(index, targetAttribute) {
      if (this.items_AO[index].type === "array") {
        // If 'array' is selected, initialize the array with an empty string
        this.resultArrays[index] = [this.items_AO[index].type];
      }
      this.setOrUpdateTargetElementData(targetAttribute, this.resultArrays.flat());
    },
    handleFieldChange(index, targetAttribute) {
      // If a non-'array' value is selected, push the values into the array
      if (this.items_AO[index].type !== "array") {
        this.resultArrays[index] = [
          `${this.items_AO[index].type}:${this.items_AO[index].field}`,
        ];
      }
      this.setOrUpdateTargetElementData(targetAttribute, this.resultArrays.flat());
    },
    setElementColumns(event, parentKey, targetKey, colNumber) {
      event.target.classList.add("activeBtnClass");
      const buttons = event.target.closest("div").querySelectorAll("button");
      // Iterate through buttons and remove the class from all except the current button
      console.log("f", this.targetElementData.columns[parentKey][targetKey].split(" "));
      buttons.forEach((button) => {
        if (button !== event.target) {
          button.classList.remove("activeBtnClass");
        }
      });
      if (targetKey == "container") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.classList.remove(value);
        }
      } else if (targetKey == "label") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.querySelector("label").classList.remove(value);
        }
      } else {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.querySelector(".form-input").classList.remove(value);
        }
      }

      if (parentKey == "tablet") {
        this.targetElementData.columns[parentKey][
          targetKey
        ] = `col-sm-${colNumber} col-md-${colNumber}`;
      } else {
        this.targetElementData.columns[parentKey][targetKey] = `col-lg-${colNumber}`;
      }

      if (targetKey == "container") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.classList.add(value);
        }
      } else if (targetKey == "label") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.querySelector("label").classList.add(value);
        }
      } else {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.querySelector(".form-input").classList.add(value);
        }
      }

      this.targetElementColumns = this.targetElementData.columns;
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
    },
    selectItem(item, targetAttribute) {
      console.log("Entering selectItem method");

      // Check if the item is not already in the array
      if (!this.uniqueSelectedItems.some((selected) => selected.id === item.id)) {
        // Create a new reference using the spread operator
        if (this.isMultiSelect) {
          // For multi-select, add the item to the array
          this.uniqueSelectedItems = [...this.uniqueSelectedItems, { ...item }];
        } else {
          // For single-select, replace the array with a new array containing only the selected item
          this.uniqueSelectedItems = [{ ...item }];
        }

        this.setOrUpdateTargetElementData(targetAttribute, this.uniqueSelectedItems);
        console.log("Item selected:", item);
        console.log("Final array:", this.uniqueSelectedItems);
      }

      console.log("Exiting selectItem method");
    },

    removeSelectedItem(selectedItem, targetAttribute) {
      this.uniqueSelectedItems = this.uniqueSelectedItems.filter(
        (item) => item.id !== selectedItem.id
      );
      this.setOrUpdateTargetElementData(targetAttribute, this.uniqueSelectedItems);
    },
    addMore1() {
      this.items.push({ htmlinnerCount: 0 });
    },
    toggleDefaultUl(event) {
      if (event.target.parentNode.nextElementSibling.style.display == "none") {
        event.target.parentNode.nextElementSibling.style.display = "block";
      } else {
        event.target.parentNode.nextElementSibling.style.display = "none";
      }
    },
    checkCondition(event) {
      const parent = event.target.parentNode.parentNode.parentNode;
      if (event.target.value === "is_not_empty" || event.target.value === "is_empty") {
        parent.querySelector(".check_conditions").classList.add("col-lg-9");
        parent.querySelector(".check_conditions").classList.remove("col-lg-3");
        parent.querySelector(".check_conditions_input").classList.add("d-none");
        console.log(`Selected value is  equal`);
      } else {
        // Show or do something else based on your requirement
        parent.querySelector(".check_conditions").classList.remove("col-lg-9");
        parent.querySelector(".check_conditions").classList.add("col-lg-3");
        parent.querySelector(".check_conditions_input").classList.remove("d-none");

        console.log(`Selected value is not equal`);
      }
    },
    addTag(event, targetAttribute) {
      const newTags = this.tagInput
        .split(",")
        .map((tag) => tag.trim())
        .filter((tag) => tag !== "");

      this.tags = [...this.tags, ...newTags];
      this.tagInput = "";
      console.log("Tags after adding:", this.tags);
      console.log("else");
      this.setOrUpdateTargetElementData(targetAttribute, this.tags);
    },
    removeTag(index, targetAttribute) {
      const removedTag = this.tags.splice(index, 1)[0];
      if (removedTag) {
        this.tagOptions.push(removedTag); // Add the removed tag back to the options
        this.setOrUpdateTargetElementData(targetAttribute, this.tags);
      }
      console.log("Tags after removing:", this.tags);
      this.setOrUpdateTargetElementData(targetAttribute, this.tags);
    },
    addTagOption(tagOption, targetAttribute) {
      // Add clicked tag option to the tags array and remove it from options
      this.tags.push(tagOption);
      const index = this.tagOptions.indexOf(tagOption);
      if (index !== -1) {
        this.tagOptions.splice(index, 1);
      }
      console.log("Tags after adding option:", this.tags);
      this.setOrUpdateTargetElementData(targetAttribute, this.tags);
    },
    addTag2(event, targetAttribute) {
      const newTags = this.tagInput2
        .split(",")
        .map((tag) => tag.trim())
        .filter((tag) => tag !== "");

      this.tags2 = [...this.tags2, ...newTags];
      this.tagInput2 = "";
      console.log("Tags after adding:", this.tags2);
      console.log("else");
      this.setOrUpdateTargetElementData(targetAttribute, this.tags2);
    },
    removeTag2(index, targetAttribute) {
      const removedTag = this.tags2.splice(index, 1)[0];
      if (removedTag) {
        this.tagOptions2.push(removedTag); // Add the removed tag back to the options
        this.setOrUpdateTargetElementData(targetAttribute, this.tags2);
      }
      console.log("Tags after removing:", this.tags2);
      this.setOrUpdateTargetElementData(targetAttribute, this.tags2);
    },
    addTagOption2(tagOption, targetAttribute) {
      // Add clicked tag option to the tags array and remove it from options
      this.tags2.push(tagOption);
      const index = this.tagOptions2.indexOf(tagOption);
      if (index !== -1) {
        this.tagOptions2.splice(index, 1);
      }
      console.log("Tags after adding option:", this.tags2);
      this.setOrUpdateTargetElementData(targetAttribute, this.tags2);
    },
    checkDisplay(event) {
      if (event.target.parentNode.nextElementSibling.style.display == "none") {
        event.target.parentNode.nextElementSibling.style.display = "block";
      } else {
        event.target.parentNode.nextElementSibling.style.display = "none";
      }
    },
    checkDisplay2(event) {
      if (event.target.parentNode.nextElementSibling.style.display == "none") {
        event.target.parentNode.nextElementSibling.style.display = "block";
      } else {
        event.target.parentNode.nextElementSibling.style.display = "none";
      }
    },
    addHtmlInner(index) {
      this.items[index].htmlinnerCount++;
    },
    addCondition(event) {
      event.target.parentNode.previousElementSibling.classList.remove("d-none");
      event.target.parentNode.classList.add("d-none");
    },
    removeHtmlMain(event, index) {
      const mainId = "main-condition-" + index;
      const mainIndex = this.items.findIndex((item) => item.id === mainId);
      this.items.splice(mainIndex, 1);
    },
    removeHtmlInner(mainIndex, subIndex) {
      // Check if htmlinnerCount is greater than 0 before removing
      if (this.items[mainIndex].htmlinnerCount > 0) {
        this.items[mainIndex].htmlinnerCount--;

        // Optionally, you may want to check if subIndex is within bounds
        if (subIndex >= 0 && subIndex < this.items[mainIndex].htmlinnerCount) {
          // Remove the specific inner item at subIndex if needed
          // this.items[mainIndex].htmlinnerItems.splice(subIndex, 1);
        }
      }
    },
    setSelectElementColumns(event, parentKey, targetKey, colNumber) {
      event.target.classList.add("activeBtnClass");
      const buttons = event.target.closest("div").querySelectorAll("button");
      // Iterate through buttons and remove the class from all except the current button

      buttons.forEach((button) => {
        if (button !== event.target) {
          button.classList.remove("activeBtnClass");
        }
      });
      if (targetKey == "container") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.classList.remove(value);
        }
      } else if (targetKey == "label") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          console.log("targetElementParent", this.targetElementParent);
          this.targetElementParent.querySelector("label").classList.remove(value);
        }
      } else {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.querySelector("select").classList.remove(value);
        }
      }

      if (parentKey == "tablet") {
        this.targetElementData.columns[parentKey][
          targetKey
        ] = `col-sm-${colNumber} col-md-${colNumber}`;
      } else {
        this.targetElementData.columns[parentKey][targetKey] = `col-lg-${colNumber}`;
      }

      if (targetKey == "container") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.classList.add(value);
        }
      } else if (targetKey == "label") {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.querySelector("label").classList.add(value);
        }
      } else {
        for (const value of this.targetElementData.columns[parentKey][targetKey].split(
          " "
        )) {
          this.targetElementParent.querySelector("select").classList.add(value);
        }
      }

      this.targetElementColumns = this.targetElementData.columns;
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
    },
    extractAttributes(element) {
      return element ? element.customAttributes : [];
    },
    setMuiltiSelect(event, targetAttribute) {
      const parent = this.targetElementParent.querySelector(
        ".multiselect-data-container"
      );
      if (targetAttribute == "name") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "label") {
        parent.querySelector("label").innerText = event.target.value;
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "label") {
        parent.querySelector("label").innerText = event.target.value;
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "title") {
        this.targetElement.setAttribute("title", event.target.value);
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "placeholder") {
        this.targetElement.placeholder = event.target.value;
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "description") {
        parent.querySelector(".vfb-preview-element-main-wrapper-desc-Upload").innerText =
          event.target.value;
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "isNative") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "isSearch") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute("readonly", "true");
        } else {
          this.targetElement.removeAttribute("readonly");
          this.setOrUpdateTargetElementData(targetAttribute, "false");
        }
      } else if (targetAttribute == "isStrictSearch") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute("readonly", "true");
        } else {
          this.targetElement.removeAttribute("readonly");
          this.setOrUpdateTargetElementData(targetAttribute, "false");
        }
      } else if (targetAttribute == "deselect") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "isClear") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "closeOnSelect") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "hideSelected") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "trackByKey") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "field_name") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "min_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "max_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "exact_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "displayCaret") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          parent.querySelector(".carret").classList.remove("d-none");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          parent.querySelector(".carret").classList.add("d-none");
        }
      } else if (targetAttribute == "truncate") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
        } else this.setOrUpdateTargetElementData(targetAttribute, "false");
      } else if (targetAttribute == "required") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
        } else this.setOrUpdateTargetElementData(targetAttribute, "false");
      } else if (targetAttribute == "nullable") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
        } else this.setOrUpdateTargetElementData(targetAttribute, "false");
      } else if (targetAttribute == "object_value") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
        } else this.setOrUpdateTargetElementData(targetAttribute, "false");
      } else if (targetAttribute == "submit_data") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
        } else this.setOrUpdateTargetElementData(targetAttribute, "false");
      } else if (targetAttribute == "before") {
        parent.querySelector(
          ".vfb-preview-element-main-wrapper-before-Upload"
        ).innerText = event.target.value;
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "between") {
        parent.querySelector(
          ".vfb-preview-element-main-wrapper-between-Upload"
        ).innerText = event.target.value;
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "after") {
        parent.querySelector(".vfb-preview-element-main-wrapper-after-Upload").innerText =
          event.target.value;
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      }
    },
    addAttributes() {
      let attributes = this.targetElementData.customAttributes;
      attributes.push({
        name: "",
        value: "",
      });
      this.targetElementData.customAttributes = attributes;
    },
    addOption() {
      let attributes = this.targetElementData.options;
      attributes.push({
        name: "",
        value: "",
      });
      this.targetElementData.options = attributes;
      this.options = this.targetElementData.options;
    },
    addModeCondition() {
      this.items.push(this.items.length + 1);
    },
    addModeInnerCondition() {
      this.items1.push(this.items.length + 1);
    },
    closeParent(index) {
      this.attributes.splice(index, 1);
    },
    makeElementCustomAttribute(event) {
      let parentElement = event.target.closest("div.checkclosehover");
      let value = parentElement.querySelector(".valueInput").value;
      let label = parentElement.querySelector(".labelInput").value;
      const index = this.targetElementData.customAttributes.findIndex(
        (obj) => obj.name == label
      );
      let keyName = "customAttributes";
      if (index !== -1) {
        // Object with the specified key exists, update it
        this.targetElementData.customAttributes[index] = { name: label, value: value };
      } else {
        // Object with the specified key doesn't exist, add it
        this.targetElementData.customAttributes.push({ name: label, value: value });
      }

      this.targetElementData.customAttributes = this.targetElementData.customAttributes.filter(
        (obj) => obj.name !== ""
      );

      this.targetElementData = {
        ...this.targetElementData,
        [keyName]: this.targetElementData.customAttributes,
      };

      this.targetElement.setAttribute(label, value);
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
    },
    makeSelectElemenOptions(event) {
      let parentElement = event.target.closest("div.checkclosehover");
      let value = parentElement.querySelector(".valueInput").value;
      let newLabel = parentElement.querySelector(".labelInput").value;
      const index = this.targetElementData.options.findIndex(
        (obj) => obj.name == newLabel
      );
      let keyName = "options";
      if (index !== -1) {
        // Object with the specified key exists, update it
        this.targetElementData.options[index] = { name: newLabel, value: value };
      } else {
        // Object with the specified key doesn't exist, add it
        this.targetElementData.options.push({ name: newLabel, value: value });
      }

      this.targetElementData.options = this.targetElementData.options.filter(
        (obj) => obj.name !== ""
      );

      this.targetElementData = {
        ...this.targetElementData,
        [keyName]: this.targetElementData.options,
      };
      this.options = this.targetElementData.options;
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
      this.targetElementParent.querySelector("ul").innerHTML = "";

      var _fnSelectAll = function (e) {
        var inputs = list.getElementsByTagName("input");
        for (var i = 0; i < inputs.length; i++) {
          if (!inputs[i].checked) {
            inputs[i].parentNode.click();
          }
        }
        e.stopPropagation();
      };

      var _selectionText = function (element) {
        var text = "";
        var selection = element.querySelectorAll("input:checked");
        if (selection.length === 0) {
          text = labels.emptyText;
        } else if (selection.length > 5) {
          text = selection.length + " " + labels.selectedText;
        } else {
          var arr = [];
          for (var i = 0; i < selection.length; i++) {
            arr.push(selection[i].parentNode.textContent);
          }
          text = arr.join(",");
        }
        return text;
      };

      var updateOrAddObject = (elementObj) => {
        if (this.tab) {
          if (typeof this.finalArr === "object" && !Array.isArray(this.finalArr)) {
            // let targetTabData = {...this.finalArr,[targetTabKey]:updateOrAddObject}
            let targetKey = this.targetTabKey;
            let targetTabData = this.finalArr.targetKey;
            if (targetTabData == undefined) {
              targetTabData = this.targetTabData;
            }
            const index = targetTabData.elements.findIndex(
              (obj) => obj.identification === elementObj.identification
            );
            if (index !== -1) {
              // Object with the specified id exists, update it
              targetTabData.elements[index] = elementObj;
            } else {
              // Object with the specified id doesn't exist, add it
              targetTabData.elements.push(elementObj);
            }
            this.finalArr = { ...this.finalArr, [this.targetTabKey]: targetTabData };
          }
        } else {
          if (Array.isArray(this.finalArr)) {
            const index = this.finalArr.findIndex(
              (obj) => obj.identification === elementObj.identification
            );
            if (index !== -1) {
              // Object with the specified id exists, update it
              this.finalArr[index] = elementObj;
            } else {
              // Object with the specified id doesn't exist, add it
              this.finalArr.push(elementObj);
            }
          } else {
            this.finalArr = [];
            this.finalArr.push(elementObj);
          }

          this.$refs.finalArrParentElement.innerHTML = `<pre>${JSON.stringify(
            this.finalArr,
            null,
            2
          )}</pre>`;
        }
      };
      var selectCb = function (data) {
        console.log(data);
      };

      var targetElementParent = this.targetElementParent;
      var targetElementData = this.targetElementData;
      var _selectItem = function () {
        var text = _selectionText(targetElementParent);
        targetElementParent
          .getElementsByTagName("button")[0]
          .children[0].setAttribute("placeholder", text);
        let selected = "selected";
        targetElementData = { ...targetElementData, [selected]: text };
        updateOrAddObject(targetElementData);
        if (this.options) {
          var selectionElements = this.targetElmentParent.querySelectorAll(
            "input:checked"
          );
          var selection = [];
          for (var i = 0; i < selectionElements.length; i++) {
            selection.push(selectionElements[i].value);
          }
          selectCb(selection);
        }
      };

      for (var i = -1; i < this.options.length; i++) {
        var item = document.createElement("li");
        var a = document.createElement("a");
        var label = document.createElement("label");
        var input = document.createElement("input");

        a.setAttribute("tabindex", "0");

        label.classList.add("multiselect-item-label");

        if (i == -1) {
          a.addEventListener("click", _fnSelectAll);
          label.appendChild(document.createTextNode("Select all"));
          label.classList.add("multiselect-item-label--select-all");
        } else {
          if (i == 0) {
            label.classList.add("multiselect-item-label--active");
          }
          input.setAttribute("type", "checkbox");
          input.setAttribute("class", "multiselect-checkbox");
          label.appendChild(input);
          input.setAttribute("value", this.options[i].value);
          input.addEventListener("change", _selectItem);
          label.appendChild(document.createTextNode(this.options[i].name));
        }
        a.appendChild(label);
        item.appendChild(a);
        targetElementParent.querySelector("ul").appendChild(item);
      }
    },
    // Function to check if the option is already appended
    isOptionAppended(option) {
      return Array.from(this.targetElementData.options).some(
        (existingOption) => existingOption.value === option.value
      );
    },
    removeElementCustomAttribute(event, index) {
      let parentElement = event.target.closest("div.checkclosehover");
      let label = parentElement.querySelector(".labelInput").value;
      delete this.targetElementCustomAttributes.label;
      let keyName = "customAttributes";
      this.targetElementData = {
        ...this.targetElementData,
        [keyName]: this.targetElementCustomAttributes,
      };

      this.targetElement.removeAttribute(label);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
      this.attributes.splice(index, 1);
    },
    removeSelectOption(event, index) {
      let options = this.targetElementData.options;
      options.splice(index, 1);
      this.targetElementData.options = options;
      this.options = options;
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
      this.targetElement.innerHTML = "";
      this.options.forEach((option) => {
        // Check if the option is already appended
        if (!this.isOptionAppended(option)) {
          const optionElement = document.createElement("option");
          optionElement.value = option.value;
          optionElement.text = option.name;
          this.targetElement.appendChild(optionElement);
        }
      });
    },
    updateOrAddObject(elementObj) {
      if (this.tab) {
        if (typeof this.finalArr === "object" && !Array.isArray(this.finalArr)) {
          // let targetTabData = {...this.finalArr,[targetTabKey]:updateOrAddObject}
          let targetKey = this.targetTabKey;
          let targetTabData = this.finalArr.targetKey;
          if (targetTabData == undefined) {
            targetTabData = this.targetTabData;
          }
          const index = targetTabData.elements.findIndex(
            (obj) => obj.identification === elementObj.identification
          );
          if (index !== -1) {
            // Object with the specified id exists, update it
            targetTabData.elements[index] = elementObj;
          } else {
            // Object with the specified id doesn't exist, add it
            targetTabData.elements.push(elementObj);
          }
          this.finalArr = { ...this.finalArr, [this.targetTabKey]: targetTabData };
        }
      } else {
        if (Array.isArray(this.finalArr)) {
          const index = this.finalArr.findIndex(
            (obj) => obj.identification === elementObj.identification
          );
          if (index !== -1) {
            // Object with the specified id exists, update it
            this.finalArr[index] = elementObj;
          } else {
            // Object with the specified id doesn't exist, add it
            this.finalArr.push(elementObj);
          }
        } else {
          this.finalArr = [];
          this.finalArr.push(elementObj);
        }

        this.$refs.finalArrParentElement.innerHTML = `<pre>${JSON.stringify(
          this.finalArr,
          null,
          2
        )}</pre>`;
      }
    },

    setOrUpdateTargetElementData(key, value) {
      const data = this.targetElement.getAttribute("data");
      this.targetElementData = data == "" ? {} : JSON.parse(data);
      this.targetElementData = {
        ...this.targetElementData,
        [key]: value,
      };
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
    },
    setElementSizeAttribute(event, targetAttribute, value) {
      this.setOrUpdateTargetElementData(targetAttribute, value);
      this.targetElementParent.classList.remove(
        "font-sm",
        "font-md",
        "font-lg",
        "font-default"
      );
      this.targetElementParent.classList.add(value);
      this.targetElement.setAttribute(targetAttribute, value);
    },
    setElementSizeAttributeImage(event, targetAttribute, value) {
      this.setOrUpdateTargetElementData(targetAttribute, value);
      this.targetElementParent.classList.remove(
        "font-sm",
        "font-md",
        "font-lg",
        "font-default"
      );
      this.targetElementParent.classList.add(value);
      this.targetElement.setAttribute(targetAttribute, value);
    },
    setElementAlignmentImage(event, targetAttribute, value) {
      this.setOrUpdateTargetElementData(targetAttribute, value);
      let element = this.targetElementParent.querySelector(".form-static-tag-img");
      element.classList.remove(element.getAttribute("data-alignment"));
      element.setAttribute("data-alignment", value);
      element.classList.add(value);
      this.targetElement.setAttribute(targetAttribute, value);
    },
    setElementSpaceTopImage(event, targetAttribute, value) {
      this.setOrUpdateTargetElementData(targetAttribute, value);
      let element = this.targetElementParent.querySelector(".form-static-tag-img");
      element.classList.remove(element.getAttribute("space-top"));
      element.setAttribute("space-top", value);
      element.classList.add(value);
      this.targetElement.setAttribute(targetAttribute, value);
    },
    setElementSpaceBottomImage(event, targetAttribute, value) {
      this.setOrUpdateTargetElementData(targetAttribute, value);
      let element = this.targetElementParent.querySelector(".form-static-tag-img");
      element.classList.remove(element.getAttribute("space-bottom"));
      element.setAttribute("space-bottom", value);
      element.classList.add(value);
      this.targetElement.setAttribute(targetAttribute, value);
    },
    setElementAttributeMultiSelect(event, targetAttribute) {
      if (targetAttribute == "before") {
        console.log(this.targetElementParent);
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-before-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "after") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-after-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "between") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-between-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "description") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-description-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "field_name") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "required") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElementParent
            .querySelector("select")
            .setAttribute("required", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElementParent
            .querySelector("select")
            .setAttribute("required", "false");
        }
      } else if (targetAttribute == "nullable") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "min_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "max_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "exact_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "object_value") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
        }
      } else if (targetAttribute == "default_value") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        const selectElement = this.targetElementParent.querySelector("select");
        // selectElement.value = event.target.value
      } else if (targetAttribute == "submit_data") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
        }
      }
    },
    setDefaultValue(event) {
      event.target.innerHTML = this.targetElementParent.querySelector("select").innerHTML;
    },
    selectDataSource(source) {
      let keyName = "dataSource";
      this.targetElementData = {
        ...this.targetElementData,
        [keyName]: source,
      };
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
    },
    setDataSourceUrl(event) {
      let keyName = "endpoint";
      this.targetElementData = {
        ...this.targetElementData,
        [keyName]: event.target.value,
      };
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
    },
    setOptionsAsJson(event) {
      let keyName = "options";
      let json = "json";

      this.targetElementData = {
        ...this.targetElementData,
        [keyName]: JSON.parse(event.target.value),
        [json]: JSON.parse(event.target.value),
      };
      this.options = this.targetElementData.options;
      this.updateOrAddObject(this.targetElementData);
      this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
      this.targetElementParent.querySelector("ul").innerHTML = "";

      var _fnSelectAll = function (e) {
        var inputs = list.getElementsByTagName("input");
        for (var i = 0; i < inputs.length; i++) {
          if (!inputs[i].checked) {
            inputs[i].parentNode.click();
          }
        }
        e.stopPropagation();
      };

      var _selectionText = function (element) {
        var text = "";
        var selection = element.querySelectorAll("input:checked");
        if (selection.length === 0) {
          text = labels.emptyText;
        } else if (selection.length > 5) {
          text = selection.length + " " + labels.selectedText;
        } else {
          var arr = [];
          for (var i = 0; i < selection.length; i++) {
            arr.push(selection[i].parentNode.textContent);
          }
          text = arr.join(",");
        }
        return text;
      };

      var updateOrAddObject = (elementObj) => {
        if (this.tab) {
          if (typeof this.finalArr === "object" && !Array.isArray(this.finalArr)) {
            // let targetTabData = {...this.finalArr,[targetTabKey]:updateOrAddObject}
            let targetKey = this.targetTabKey;
            let targetTabData = this.finalArr.targetKey;
            if (targetTabData == undefined) {
              targetTabData = this.targetTabData;
            }
            const index = targetTabData.elements.findIndex(
              (obj) => obj.identification === elementObj.identification
            );
            if (index !== -1) {
              // Object with the specified id exists, update it
              targetTabData.elements[index] = elementObj;
            } else {
              // Object with the specified id doesn't exist, add it
              targetTabData.elements.push(elementObj);
            }
            this.finalArr = { ...this.finalArr, [this.targetTabKey]: targetTabData };
          }
        } else {
          if (Array.isArray(this.finalArr)) {
            const index = this.finalArr.findIndex(
              (obj) => obj.identification === elementObj.identification
            );
            if (index !== -1) {
              // Object with the specified id exists, update it
              this.finalArr[index] = elementObj;
            } else {
              // Object with the specified id doesn't exist, add it
              this.finalArr.push(elementObj);
            }
          } else {
            this.finalArr = [];
            this.finalArr.push(elementObj);
          }

          this.$refs.finalArrParentElement.innerHTML = `<pre>${JSON.stringify(
            this.finalArr,
            null,
            2
          )}</pre>`;
        }
      };
      var selectCb = function (data) {
        console.log(data);
      };

      var targetElementParent = this.targetElementParent;
      var targetElementData = this.targetElementData;
      var _selectItem = function () {
        var text = _selectionText(targetElementParent);
        targetElementParent
          .getElementsByTagName("button")[0]
          .children[0].setAttribute("placeholder", text);
        let selected = "selected";
        targetElementData = { ...targetElementData, [selected]: text };
        updateOrAddObject(targetElementData);
        if (this.options) {
          var selectionElements = this.targetElmentParent.querySelectorAll(
            "input:checked"
          );
          var selection = [];
          for (var i = 0; i < selectionElements.length; i++) {
            selection.push(selectionElements[i].value);
          }
          selectCb(selection);
        }
      };

      for (var i = -1; i < this.options.length; i++) {
        var item = document.createElement("li");
        var a = document.createElement("a");
        var label = document.createElement("label");
        var input = document.createElement("input");

        a.setAttribute("tabindex", "0");

        label.classList.add("multiselect-item-label");

        if (i == -1) {
          a.addEventListener("click", _fnSelectAll);
          label.appendChild(document.createTextNode("Select all"));
          label.classList.add("multiselect-item-label--select-all");
        } else {
          if (i == 0) {
            label.classList.add("multiselect-item-label--active");
          }
          input.setAttribute("type", "checkbox");
          input.setAttribute("class", "multiselect-checkbox");
          label.appendChild(input);
          input.setAttribute("value", this.options[i].value);
          input.addEventListener("change", _selectItem);
          label.appendChild(document.createTextNode(this.options[i].name));
        }
        a.appendChild(label);
        item.appendChild(a);
        targetElementParent.querySelector("ul").appendChild(item);
      }
    },
    setElementAttribute(event, targetAttribute) {
      this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      if (targetAttribute == "prefix") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".form-input .vfb-preview-element-inner-wrapper-before"
        ).innerText = event.target.value;
      } else if (targetAttribute == "suffix") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".form-input .vfb-preview-element-inner-wrapper-after"
        ).innerText = event.target.value;
      } else if (targetAttribute == "before") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-before"
        ).innerText = event.target.value;
      } else if (targetAttribute == "between") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-between"
        ).innerText = event.target.value;
      } else if (targetAttribute == "after") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-after"
        ).innerText = event.target.value;
      } else if (targetAttribute == "floating") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".form-input .form-input-Main .vfb-floating-span"
        ).innerText = event.target.value;
      } else if (targetAttribute == "type") {
        // this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector("input").type = event.target.value;
      }
    },
    setTabName(event) {
      this.targetTabData.name = event.target.value;
      document.querySelector(".tab.active").textContent = this.targetTabData.name;
      let currentTab = this.targetTabKey;
      this.finalArr[currentTab] = this.targetTabData;
      document
        .querySelector(".tab.active")
        .setAttribute("data", JSON.stringify(this.targetTabData));
    },
    setElementiImageAttribute(event, targetAttribute) {
      if (targetAttribute == "name") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        // this.targetElementParent.querySelector('.vfb-preview-element-name-tag').innerText = event.target.value
      } else if (targetAttribute == "label") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector("label").innerText = event.target.value;
      } else if (targetAttribute == "title") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent
          .querySelector("label")
          .setAttribute("title", event.target.value);
      } else if (targetAttribute == "description") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-desc-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "imgurl") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector("img").src = event.target.value;
      } else if (targetAttribute == "alt") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector("img").alt = event.target.value;
      } else if (targetAttribute == "inputtitle") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent
          .querySelector("img")
          .setAttribute("title", event.target.value);
      } else if (targetAttribute == "width") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent
          .querySelector("img")
          .setAttribute("width", event.target.value);
      } else if (targetAttribute == "height") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent
          .querySelector("img")
          .setAttribute("height", `${event.target.value}px`);
      } else if (targetAttribute == "linkurl") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent
          .querySelector("a")
          .setAttribute("href", event.target.value);
      } else if (targetAttribute == "target") {
        this.targetElementParent
          .querySelector("a")
          .setAttribute("target", event.target.value);
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
      } else if (targetAttribute == "before") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-before-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "between") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-between-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "after") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-after-Upload"
        ).innerText = event.target.value;
      }
    },
    setCheckboxElementAttribute(event, targetAttribute) {
      this.setOrUpdateTargetElementData(targetAttribute, event.target.checked);
      this.targetElement.setAttribute(targetAttribute, event.target.checked);
    },
    showModel() {
      document.getElementById("exampleModal").classList.add("show");
      document.getElementById("exampleModal").style.display = "block";
    },
    closeModel(event) {
      document.getElementById("exampleModal").classList.remove("show");
      document.getElementById("exampleModal").style.display = "";
      event.target.parentNode.parentNode.previousElementSibling.previousElementSibling.classList.add(
        "d-none"
      );
      event.target.parentNode.parentNode.previousElementSibling.classList.remove(
        "d-none"
      );
    },

    setElementLabel(event) {
      if (this.targetElementParent.querySelector("label") != null) {
        this.setOrUpdateTargetElementData("label", event.target.value);
        this.targetElementParent.querySelector("label").textContent = event.target.value;
      }
    },
    setLabelTooltip(event) {
      if (this.targetElementParent.querySelector("label") != null) {
        this.targetElementParent
          .querySelector("label")
          .setAttribute("title", event.target.value);
        this.setOrUpdateTargetElementData("title", event.target.value);
      }
    },
    cloneTextElement(event) {
      const clone = this.targetElementParent.querySelector(
        ".vfb-action .vfb-preview-element-actions-container .vfb-clone"
      );
      clone.click();
    },
    deleteTextElement(event) {
      const deleteEle = this.targetElementParent.querySelector(
        ".vfb-action .vfb-preview-element-actions-container .vfb-delete"
      );
      deleteEle.click();
      document.getElementById("rightMenu").style.right = "-400px";
    },
    cloneSelectElement(event) {
      const clone = this.targetElementParent.querySelector(
        ".vfb-action .vfb-preview-element-actions-container .vfb-clone"
      );
      clone.click();
    },
    deleteSelectElement(event) {
      const deleteEle = this.targetElementParent.querySelector(
        ".vfb-action .vfb-preview-element-actions-container .vfb-delete"
      );
      deleteEle.click();
      document.getElementById("multiSelectrightMenu").style.right = "-400px";
    },
    handleClick(event) {
      const currentElement = event.currentTarget;
      if (currentElement.nextElementSibling.style.display == "none") {
        currentElement.children[1].classList.add("d-none");
        currentElement.children[2].classList.remove("d-none");
        currentElement.nextElementSibling.style.display = "";
        currentElement.parentNode.style.borderBottom = "0px";
        const iconPlusElements = document.querySelectorAll(".vv-vfb-icon-plus");
        const iconCloseElements = document.querySelectorAll(".vv-vfb-icon-close");
        iconCloseElements.forEach((iconClose) => {
          iconClose.classList.remove("d-none");
        });
        iconPlusElements.forEach((iconPlus) => {
          iconPlus.classList.add("d-none");
        });
      } else {
        currentElement.nextElementSibling.style.display = "none";
        currentElement.children[1].classList.remove("d-none");
        currentElement.children[2].classList.add("d-none");
        currentElement.parentNode.style.borderBottom = "1px solid rgb(236 240 244 / 1)";
        const iconPlusElements = document.querySelectorAll(".vv-vfb-icon-plus");
        const iconCloseElements = document.querySelectorAll(".vv-vfb-icon-close");
        iconPlusElements.forEach((iconPlus) => {
          iconPlus.classList.remove("d-none");
        });
        iconCloseElements.forEach((iconClose) => {
          iconClose.classList.add("d-none");
        });
      }
    },

    ColapsToggleExpand() {
      // Get all elements with the class 'vfb-faqs-body'
      const elements = document.querySelectorAll(".vfb-faqs-body");

      // Get all elements with the classes 'vv-vfb-icon-plus' and 'vv-vfb-icon-close'
      const iconPlusElements = document.querySelectorAll(".vv-vfb-icon-plus");
      const iconCloseElements = document.querySelectorAll(".vv-vfb-icon-close");

      // Get all elements with the classes 'vfb-config-form-header-collapse-open' and 'vfb-config-form-header-collapse-close'
      const headerOpenElements = document.querySelectorAll(
        ".vfb-config-form-header-collapse-open"
      );
      const headerCloseElements = document.querySelectorAll(
        ".vfb-config-form-header-collapse-close"
      );

      // Iterate through the elements
      elements.forEach((element) => {
        // Check the current display property
        const currentDisplay = window
          .getComputedStyle(element)
          .getPropertyValue("display");

        // Toggle the display property (reverse logic)
        if (currentDisplay === "block") {
          element.style.display = "none";
          // Show elements with class 'vv-vfb-icon-close' and hide elements with class 'vv-vfb-icon-plus' (reverse logic)
          iconCloseElements.forEach((iconClose) => {
            iconClose.classList.add("d-none");
          });
          iconPlusElements.forEach((iconPlus) => {
            iconPlus.classList.remove("d-none");
          });

          // Hide elements with class 'vfb-config-form-header-collapse-open' and show elements with class 'vfb-config-form-header-collapse-close'
          headerOpenElements.forEach((headerOpen) => {
            headerOpen.classList.add("d-none");
          });
          headerCloseElements.forEach((headerClose) => {
            headerClose.classList.remove("d-none");
          });
        } else {
          element.style.display = "block";
          // Show elements with class 'vv-vfb-icon-plus' and hide elements with class 'vv-vfb-icon-close' (reverse logic)
          iconPlusElements.forEach((iconPlus) => {
            iconPlus.classList.add("d-none");
          });
          iconCloseElements.forEach((iconClose) => {
            iconClose.classList.remove("d-none");
          });

          // Show elements with class 'vfb-config-form-header-collapse-open' and hide elements with class 'vfb-config-form-header-collapse-close'
          headerOpenElements.forEach((headerOpen) => {
            headerOpen.classList.add("d-none");
          });
          headerCloseElements.forEach((headerClose) => {
            headerClose.classList.remove("d-none");
          });
        }
      });
    },

    ColapsToggleClose() {
      // Get all elements with the class 'vfb-faqs-body'
      const elements = document.querySelectorAll(".vfb-faqs-body");

      // Get all elements with the classes 'vv-vfb-icon-plus' and 'vv-vfb-icon-close'
      const iconPlusElements = document.querySelectorAll(".vv-vfb-icon-plus");
      const iconCloseElements = document.querySelectorAll(".vv-vfb-icon-close");

      // Get all elements with the classes 'vfb-config-form-header-collapse-open' and 'vfb-config-form-header-collapse-close'
      const headerOpenElements = document.querySelectorAll(
        ".vfb-config-form-header-collapse-open"
      );
      const headerCloseElements = document.querySelectorAll(
        ".vfb-config-form-header-collapse-close"
      );

      // Iterate through the elements
      elements.forEach((element) => {
        // Set the display property to 'none'
        element.style.display = "none";
      });

      // Show elements with class 'vv-vfb-icon-plus' and hide elements with class 'vv-vfb-icon-close'
      iconPlusElements.forEach((iconPlus) => {
        iconPlus.classList.remove("d-none");
      });

      iconCloseElements.forEach((iconClose) => {
        iconClose.classList.add("d-none");
      });

      // Show elements with class 'vfb-config-form-header-collapse-open' and hide elements with class 'vfb-config-form-header-collapse-close'
      headerOpenElements.forEach((headerOpen) => {
        headerOpen.classList.remove("d-none");
      });

      headerCloseElements.forEach((headerClose) => {
        headerClose.classList.add("d-none");
      });
    },

    textClose() {
      document.getElementById("rightMenu").style.right = "-500px";
    },
    multiselectClose() {
      document.getElementById("multiSelectrightMenu").style.right = "-500px";
    },
    MultiClose() {
      document.getElementById("rightMenuMultiImage").style.right = "-500px";
    },
    ImageClose() {
      document.getElementById("rightMenuImage").style.right = "-500px";
    },
    TabsClose() {
      document.getElementById("rightMenuTab").style.right = "-500px";
    },
   
    vfbmodelarrayClose() {
      document.getElementById("vfbmodelarray").style.right = "-400px";
    },

    setFloat(event, whichBtextFieldutton) {
      if (whichButton == "off") {
        this.setOrUpdateTargetElementData("autoFloat", "off");
        event.target.parentNode.parentNode.nextElementSibling.classList.remove("d-none");
        event.target.parentNode.parentNode.nextElementSibling.classList.add("d-flex");
      } else {
        this.setOrUpdateTargetElementData("autoFloat", "default");
        event.target.parentNode.parentNode.nextElementSibling.classList.add("d-none");
        event.target.parentNode.parentNode.nextElementSibling.classList.remove("d-flex");
      }
    },
    handleInput(event) {
      document.getElementById("rightMenuMultiImage").style.right = "-500px";
      document.getElementById("rightMenu").style.right = "-500px";
      document.getElementById("multiSelectrightMenu").style.right = "-500px";
      document.getElementById("rightMenuTab").style.right = "0px";
      document.getElementById("rightMenuImage").style.right = "-500px";
      let parentElement = event.target.closest(".container-text-div");
      if (parentElement != null && parentElement.innerHTML != "") {
        const textField = parentElement.querySelector("input");
        const data = textField.getAttribute("data");
        this.targetElementData = data == "" ? {} : JSON.parse(data);
        this.targetElementCustomAttributes = this.targetElementData.customAttributes
          ? this.targetElementData.customAttributes
          : [];
        this.targetElementColumns = this.targetElementData?.columns;
        this.targetElement = textField;
        this.targetElementParent = textField.closest(".container-text-div");
        this.updateOrAddObject(this.targetElementData);
      }
    },
    handleMultiSelect(event) {
      document.getElementById("rightMenuMultiImage").style.right = "-500px";
      document.getElementById("rightMenu").style.right = "-500px";
      document.getElementById("multiSelectrightMenu").style.right = "0px";
      document.getElementById("rightMenuTab").style.right = "-500px";
      let parentElement = event.target.closest(".container-select-div");
      const textField = parentElement.querySelector("input");
      const data = textField.getAttribute("data");
      this.targetElementData = data == "" ? {} : JSON.parse(data);
      console.log("taraget elem", this.targetElementData);
      this.targetElementCustomAttributes = this.targetElementData.customAttributes
        ? this.targetElementData.customAttributes
        : [];
      this.targetElementColumns = this.targetElementData?.columns;
      this.targetElement = textField;
      this.targetElementParent = textField.closest(".container-text-div");
      this.updateOrAddObject(this.targetElementData);
    },
    handleMultiImage(event) {
      let parentElement = event.target.closest("div.containerUploadDiv");
      const textField = parentElement.querySelector("input");
      const data = textField.getAttribute("data");
      this.targetElementData = data == "" ? {} : JSON.parse(data);
      console.log("taraget elem", this.targetElementData);
      this.targetElementCustomAttributes = this.targetElementData.customAttributes
        ? this.targetElementData.customAttributes
        : [];
      this.targetElementColumns = this.targetElementData?.columns;
      this.targetElement = textField;
      this.targetElementParent = textField.closest("div.containerUploadDiv");
      document.getElementById("rightMenuMultiImage").style.right = "0px";
      document.getElementById("rightMenu").style.right = "-500px";
      document.getElementById("multiSelectrightMenu").style.right = "-500px";
      document.getElementById("rightMenuTab").style.right = "-500px";
      document.getElementById("rightMenuImage").style.right = "-500px";

      this.updateOrAddObject(this.targetElementData);
    },
    handleSelect(event) {
      let parentElement = event.target.closest(".multiselect-container");
      document.getElementById("multiSelectrightMenu").style.right = "0px";
      document.getElementById("rightMenu").style.right = "-500px";
      document.getElementById("rightMenuTab").style.right = "-500px";
      document.getElementById("rightMenuMultiImage").style.right = "-500px";
      document.getElementById("rightMenuImage").style.right = "-500px";
      if (parentElement != null && parentElement.innerHTML != "") {
        const selectField = parentElement.querySelector("button input");
        const data = selectField.getAttribute("data");
        this.targetElementData = data == "" ? {} : JSON.parse(data);
        this.targetElementCustomAttributes = this.targetElementData.customAttributes
          ? this.targetElementData.customAttributes
          : [];
        this.targetElementColumns = this.targetElementData?.columns;
        this.options = this.targetElementData?.options;
        this.targetElement = selectField;
        this.targetElementParent = event.target.closest(".multiselect-container");
        this.targetElementColumns = this.targetElementData.columns;
        this.updateOrAddObject(this.targetElementData);
        this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
      }
    },
    handleImage(event) {
      document.getElementById("rightMenuImage").style.right = "0px";
      document.getElementById("rightMenuMultiImage").style.right = "-500px";
      document.getElementById("rightMenu").style.right = "-500px";
      document.getElementById("multiSelectrightMenu").style.right = "-500px";
      document.getElementById("rightMenuTab").style.right = "-500px";

      let parentElement = event.target.closest("div.containerImageUploadDiv");
      const imgField = parentElement.querySelector("img");
      const data = imgField.getAttribute("data");
      this.targetElementData = data == "" ? {} : JSON.parse(data);
      // console.log("taraget elem img", this.parentElement);
      this.targetElementCustomAttributes = this.targetElementData.customAttributes
        ? this.targetElementData.customAttributes
        : [];
      this.targetElementColumns = this.targetElementData?.columns;
      this.targetElement = imgField;
      this.targetElementParent = imgField.closest("div.containerImageUploadDiv");
      // console.log("taraget elem img", this.targetElementParent);
      document.getElementById("rightMenuMultiImage").style.right = "0px";
      document.getElementById("rightMenu").style.right = "-500px";
      document.getElementById("multiSelectrightMenu").style.right = "-500px";
      console.log(this.targetElementParent);
      this.updateOrAddObject(this.targetElementData);
    },
    setElementMultiImageAttribute(event, targetAttribute) {
      if (targetAttribute == "name") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
        console.log(this.targetElement);
        this.targetElementParent.querySelector(
          ".hoverableUpload .vfb-action .vfb-preview-element-name-tag-div label"
        ).innerText = event.target.value;
      } else if (targetAttribute == "label") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
        console.log( this.targetElementParent.querySelector("label"))
        this.targetElementParent.querySelector("label").innerText = event.target.value;
      } else if (targetAttribute == "tooltip") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
        this.targetElementParent
          .querySelector("label")
          .setAttribute("title", event.target.value);
      } else if (targetAttribute == "desc") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-desc-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "click_urls") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "preview_urls") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "file_key") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "before") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-before-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "after") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-after-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "between") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
        this.targetElementParent.querySelector(
          ".vfb-preview-element-main-wrapper-between-Upload"
        ).innerText = event.target.value;
      } else if (targetAttribute == "field_name") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "min_file_size") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "extensions") {
        var selectElement1 = event.target;
        var selectedValues1 = [];

        for (var i = 0; i < selectElement1.options.length; i++) {
          if (selectElement1.options[i].selected) {
            selectedValues1.push(selectElement1.options[i].value);
          }
        }

        this.setOrUpdateTargetElementData(targetAttribute, selectedValues1.join(", "));
        this.targetElement.setAttribute(targetAttribute, selectedValues1.join(", "));
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "min_height") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "width") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "height") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "min_width") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "ratio") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "required") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "nullable") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "min_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "exact_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "max_file_size") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "max_width") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "max_height") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute == "max_items") {
        this.setOrUpdateTargetElementData(targetAttribute, event.target.value);
        this.targetElement.setAttribute(targetAttribute, event.target.value);
      } else if (targetAttribute === "inputId") {
        let previousId = this.targetElementParent.querySelector("input").id;

        // If event.target.value is not null or an empty string, use it; otherwise, use the previousId
        previousId =
          event.target.value !== null && event.target.value !== ""
            ? event.target.value
            : previousId;

        this.setOrUpdateTargetElementData(targetAttribute, previousId);
        this.targetElement.setAttribute(targetAttribute, previousId);
      }
    },
    // },
    autoUpload(event, targetAttribute) {
      if (targetAttribute == "autoupload") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("Auto-Upload", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("Auto-Upload", "false");
        }
      } else if (targetAttribute == "dragdrop") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("Drag-Drop", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("Drag-Drop", "false");
        }
      } else if (targetAttribute == "softremove") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("softremove", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("softremove", "false");
        }
      } else if (targetAttribute == "clickable") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("clickable", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("clickable", "false");
        }
      } else if (targetAttribute == "control_can_add") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("control_can_add", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("control_can_add", "false");
        }
      } else if (targetAttribute == "control_can_remove") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("control_can_remove", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("control_can_remove", "false");
        }
      } else if (targetAttribute == "control_can_sort") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("control_can_sort", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("control_can_sort", "false");
        }
      } else if (targetAttribute == "submit_data") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("submit_data", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("submit_data", "false");
        }
      } else if (targetAttribute == "disabled") {
        if (event.target.checked == true) {
          this.setOrUpdateTargetElementData(targetAttribute, "true");
          this.targetElement.setAttribute(targetAttribute, "true");
          this.targetElementParent
            .querySelector("input")
            .setAttribute("disabled", "true");
        } else {
          this.setOrUpdateTargetElementData(targetAttribute, "false");
          this.targetElement.setAttribute(targetAttribute, "false");
          this.targetElementParent
            .querySelector("input")
            .removeAttribute("disabled", "false");
        }
      }
    },
    getSelectedOptions(event, targetAttribute) {},
    setAccept(event, targetAttribute, type) {
      const index = this.acceptedTypes.indexOf(type);
      if (index === -1) {
        // Type not in the array, add it
        this.acceptedTypes.push(type);
      } else {
        // Type already in the array, remove it
        this.acceptedTypes.splice(index, 1);
      }

      // Update the input element dynamically
      const fileInput = this.targetElementParent.querySelector("input");
      if (fileInput) {
        fileInput.accept = this.acceptedTypes.join(",");
      }
      const finalArray = this.acceptedTypes;
      this.setOrUpdateTargetElementData(targetAttribute, finalArray);
      this.targetElement.setAttribute(targetAttribute, finalArray);
    },
    customDropdown(event) {
      console.log(event);
    },
    handleDragStart(event) {
      event.dataTransfer.setData("text/plain", event.target.getAttribute("data-code"));
    },
    handleDragOver(event) {
      // console.log("handleDragOver");

      event.preventDefault();
      const dropContainer = document.getElementById("drop-container");
      dropContainer.classList.add("row");
      dropContainer.style.backgroundColor = "#d1fae5";
    },
    checkedColumns(event) {
      const parentElement = event.target.closest("div.tab-pane");
      if (!event.target.checked) {
        parentElement.querySelector(".tab-inner-content").classList.remove("d-none");
      } else {
        parentElement.querySelector(".tab-inner-content").classList.add("d-none");
      }
    },

    async selectTab(event) {
      this.targetTabData = JSON.parse(event.target.getAttribute("data"));
      this.targetTabKey = this.targetTabData.uniqueKey;
      this.currentTabID = event.target.getAttribute("data-id");
      let parentDiv = event.target.closest("div.tabsParentDiv");
      await document.querySelectorAll(".tabs").forEach(function (tabContainer) {
        tabContainer.querySelectorAll("div").forEach(function (tab) {
          tab.classList.remove("active");
        });
      });
      event.currentTarget.classList.add("active");
      await document
        .querySelectorAll(".tab-content-container")
        .forEach(function (tabContentContainer) {
          tabContentContainer.querySelector("div").classList.add("d-none");
        });
      parentDiv.querySelector(`#${this.currentTabID}`).classList.remove("d-none");
    },
    createNewTab() {
      this.tabsCount++;
      this.tab = true;
      let tabName = "Tab " + this.tabsCount;
      let uniqueKey = "Tab" + this.tabsCount;
      // this.currentTabID = "tab-content-1";
      this.tabs.push(tabName);
      // Main container for tabs and content
      let dropContainer = document.getElementById("drop-container");
      if (this.tabsCount == 1) {
        let tabsParentDiv = document.createElement("div");
        tabsParentDiv.classList.add("tabsParentDiv");
        tabsParentDiv.id = "tabsParentDiv";
        // Create the main tabs container
        const tabsNameContainer = document.createElement("div");
        tabsNameContainer.className = "tabs";
        tabsNameContainer.id = "tabsNameContainer";
        // Create a container for tab content areas
        const tabContentContainer = document.createElement("div");
        tabContentContainer.className = "tab-content-container";
        const tabContent = document.createElement("div");
        tabContent.id = `tab-content-${this.tabsCount}`;
        this.currentTabID = `tab-content-${this.tabsCount}`;
        // tabContent.textContent = `Content for Tab ${this.tabsCount}`; // Placeholder text
        tabContentContainer.appendChild(tabContent);

        const tab = document.createElement("div");

        this.targetTabKey = uniqueKey;
        this.targetTabData = {
          uniqueKey: this.targetTabKey,
          name: tabName,
          elements: [],
        };
        tab.setAttribute("data", JSON.stringify(this.targetTabData));
        tab.className = "tab";
        tab.textContent = this.targetTabData.name;
        tab.classList.add("active");
        tab.setAttribute("data-id", `tab-content-${this.tabsCount}`);
        tab.addEventListener("click", this.selectTab);
        var ttabMainContainer = document.createElement("div");
        // ttabMainContainer.onclick = this.selectTab;
        ttabMainContainer.addEventListener("click", this.selectTab);

        ttabMainContainer.className =
          "position-absolute justify-content-between w-100 vfb-action";

        // Set identification property for ttabMainContainer
        // ttabMainContainer.identification = "mainContainer_" + this.tabsCount;

        // Create the first child
        var ttabSVGTagDiv = document.createElement("div");
        ttabSVGTagDiv.className = "vfb-preview-element-svg-tag-div";

        var ttabNameLabel = document.createElement("label");
        ttabNameLabel.className = "vfb-clone";
        ttabNameLabel.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path class="" fill="currentColor" d="M493.26 56.26l-37.51-37.51C443.25 6.25 426.87 0 410.49 0s-32.76 6.25-45.25 18.74l-74.49 74.49L256 127.98 12.85 371.12.15 485.34C-1.45 499.72 9.88 512 23.95 512c.89 0 1.79-.05 2.69-.15l114.14-12.61L384.02 256l34.74-34.74 74.49-74.49c25-25 25-65.52.01-90.51zM118.75 453.39l-67.58 7.46 7.53-67.69 231.24-231.24 31.02-31.02 60.14 60.14-31.02 31.02-231.33 231.33zm340.56-340.57l-44.28 44.28-60.13-60.14 44.28-44.28c4.08-4.08 8.84-4.69 11.31-4.69s7.24.61 11.31 4.69l37.51 37.51c6.24 6.25 6.24 16.4 0 22.63z"></path><!--v-if--></svg>
`;

        // Set identification property for ttabNameLabel
        // ttabNameLabel.identification = "nameLabel_" + this.elementCount;

        ttabSVGTagDiv.appendChild(ttabNameLabel);

        // Create the second child
        var ttabActionsContainer = document.createElement("div");
        ttabActionsContainer.className = "vfb-preview-element-actions-container";

        var ttabCloneDiv = document.createElement("div");
        ttabCloneDiv.className = "vfb-clone";

        ttabCloneDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zM362 464H54a6 6 0 0 1-6-6V150a6 6 0 0 1 6-6h42v224c0 26.51 21.49 48 48 48h224v42a6 6 0 0 1-6 6zm96-96H150a6 6 0 0 1-6-6V54a6 6 0 0 1 6-6h308a6 6 0 0 1 6 6v308a6 6 0 0 1-6 6z"></path></svg>
`;

        var ttabDeleteDiv = document.createElement("div");
        ttabDeleteDiv.className = "vfb-delete";

        ttabDeleteDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M268 416h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12zM432 80h-82.41l-34-56.7A48 48 0 0 0 274.41 0H173.59a48 48 0 0 0-41.16 23.3L98.41 80H16A16 16 0 0 0 0 96v16a16 16 0 0 0 16 16h16v336a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V128h16a16 16 0 0 0 16-16V96a16 16 0 0 0-16-16zM171.84 50.91A6 6 0 0 1 177 48h94a6 6 0 0 1 5.15 2.91L293.61 80H154.39zM368 464H80V128h288zm-212-48h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12z"></path></svg>
`;

        // ttabActionsContainer.appendChild(ttabCloneDiv); (abcappend)
        ttabActionsContainer.appendChild(ttabDeleteDiv);

        // Append children to the main container
        ttabMainContainer.appendChild(ttabSVGTagDiv);
        ttabMainContainer.appendChild(ttabActionsContainer);

        // Append the main container to another container (e.g., containerTextDiv)
        // tab.appendChild(ttabMainContainer);

        tabsNameContainer.appendChild(tab);
        tabsParentDiv.appendChild(tabsNameContainer);
        //let dropContainerHTML = dropContainer.innerHTML;
        //dropContainer.innerHTML='';
        //tabContentContainer.innerHTML = dropContainerHTML;
        tabsParentDiv.appendChild(tabContentContainer);
        dropContainer.insertBefore(tabsParentDiv, dropContainer.childNodes[1]);
        // dropContainer.childNodes[1] = dropContainer.prepend(tabsParentDiv);
        const plussvg = `<svg data-v-2a324127="" width="12px" height="12px" class="vfb-icon vfb-config-form-header-collapse-open" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"><path data-v-2a324127="" class="" fill="#94a3b8" d="M368 224H224V80c0-8.84-7.16-16-16-16h-32c-8.84 0-16 7.16-16 16v144H16c-8.84 0-16 7.16-16 16v32c0 8.84 7.16 16 16 16h144v144c0 8.84 7.16 16 16 16h32c8.84 0 16-7.16 16-16V288h144c8.84 0 16-7.16 16-16v-32c0-8.84-7.16-16-16-16z"></path><!--v-if--></svg>`;
        const plusIconContainer = document.createElement("div");
        plusIconContainer.innerHTML = plussvg;
        plusIconContainer.id = "plusIcon"; // Setting ID to the container

        tabsParentDiv = document.getElementById("tabsParentDiv"); // The parent element where the plus icon should be placed
        tabsParentDiv.appendChild(plusIconContainer);
        document.getElementById("plusIcon").addEventListener("click", () => {
          this.createNewTab();
        });
        // dropContainer.appendChild(tabsParentDiv);
      } else {
        const tabsParentDiv = document.getElementById("tabsParentDiv");
        const tabsNameContainer = document.getElementById("tabsNameContainer");
        // Create a container for tab content areas
        const tabContentContainer = document.createElement("div");
        tabContentContainer.className = "tab-content-container";
        const tabContent = document.createElement("div");
        tabContent.id = `tab-content-${this.tabsCount}`;
        tabContent.classList.add("d-none");
        // tabContent.textContent = `Content for Tab ${this.tabsCount}`; // Placeholder text
        tabContentContainer.appendChild(tabContent);
        const tab = document.createElement("div");

        tab.setAttribute(
          "data",
          JSON.stringify({
            uniqueKey: uniqueKey,
            name: tabName,
            elements: [],
          })
        );
        tab.className = "tab";
        tab.textContent = tabName;
        tab.setAttribute("data-id", `tab-content-${this.tabsCount}`);
        tab.addEventListener("click", this.selectTab);
        tabsNameContainer.appendChild(tab);
        tabsParentDiv.appendChild(tabContentContainer);
        dropContainer.appendChild(tabsParentDiv);
      }
    },
    removeImageInnerElement(event){
      let imageUrl = event.target.getAttribute('data-img');
      let uploadedImageUrls = this.targetElementData.urls ? this.targetElementData.urls : []
            event.stopPropagation();
            event.currentTarget.parentNode.remove();
            // Remove the corresponding imageUrl from uploadedImageUrls
            const indexToRemove = uploadedImageUrls.indexOf(imageUrl);
            if (indexToRemove !== -1) {
              uploadedImageUrls.splice(indexToRemove, 1);
            }
            let keyName = "urls";
          this.targetElementData = {
            ...this.targetElementData,
            [keyName]: uploadedImageUrls,
          };
          this.updateOrAddObject(this.targetElementData);
          this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
    },
    handleFileUpload(event) {
      var containerUploadDiv = event.target.closest('.containerUploadDiv')
      let uploadedImageUrls = this.targetElementData.urls ? this.targetElementData.urls : []
        for (const file of event.target.files) {
          const imageUrl = URL.createObjectURL(file);
          uploadedImageUrls.push(imageUrl); // Add imageUrl to the array
          const maindiv = document.createElement("div");
          const imageUrlDiv = document.createElement("div");
          const imageDiv = document.createElement("div");
          const spanclose = document.createElement("span");
          const image = document.createElement("img");
          this.imageUrl = imageUrl
          // Adding classes
          maindiv.classList.add("vfb-file-upload", "d-flex");
          imageUrlDiv.classList.add("vfb-file-url");
          spanclose.classList.add("vfb-file-closeopen");
          image.src = imageUrl;
          imageUrlDiv.innerText = imageUrl;
          // Adding click event listener to remove the parent div
          // Appending elements to maindiv
          
          spanclose.addEventListener("click", this.removeImageInnerElement);
          imageDiv.appendChild(image);
          maindiv.appendChild(imageDiv);
          maindiv.appendChild(imageUrlDiv);
          maindiv.appendChild(spanclose);
          spanclose.setAttribute('data-img',imageUrl);
          // Appending maindiv to dropContainer
          containerUploadDiv.appendChild(maindiv);
        }
        let keyName = "urls";
          this.targetElementData = {
            ...this.targetElementData,
            [keyName]: uploadedImageUrls,
          };
          this.updateOrAddObject(this.targetElementData);
          this.targetElement.setAttribute("data", JSON.stringify(this.targetElementData));
        
      //  console.log(targetInput)
  

      },
    appendSelectElement(targetData, clone) {
      var elementCount = ++this.elementCount;
      var Motus = {};
      var container;
      var createMultiselect = function createMultiselect(
        element,
        data,
        selectCb,
        options
      ) {
        var labels = {};

        labels.emptyText =
          options && options.emptyText ? options.emptyText : "Select an option";
        labels.selectedText =
          options && options.selectedText ? options.selectedText : "Selected";
        labels.selectedAllText =
          options && options.selectedAllText ? options.selectedAllText : "Select All";
        labels.title = options && options.title ? options.title : "Field";

        //define the elements
        container = document.createElement("div");
        var multiselectLabel = document.createElement("div");
        var dataContainer = document.createElement("div");

        var labelElement = document.createElement("label");
        labelElement.innerText = "Multiselect";
        var multiselectbefore = document.createElement("div");
        var multiselectafter = document.createElement("div");
        var multiselectbetween = document.createElement("div");
        var multiselectdesc = document.createElement("div");

        var button = document.createElement("button");
        var searchField = document.createElement("input");
        var clearSelection = document.createElement("span");
        var carret = document.createElement("b");
        var list = document.createElement("ul");

        //  add classes
        multiselectbefore.classList.add("vfb-preview-element-main-wrapper-before-Upload");
        multiselectafter.classList.add("vfb-preview-element-main-wrapper-after-Upload");
        multiselectbetween.classList.add(
          "vfb-preview-element-main-wrapper-between-Upload"
        );
        multiselectdesc.classList.add("vfb-preview-element-main-wrapper-desc-Upload");

        //set the ids
        var timestamp = Math.round(new Date().getTime() * Math.random());
        container.setAttribute("id", "multiselect_container_" + timestamp);
        dataContainer.setAttribute("id", "multiselect_datacontainer_" + timestamp);
        multiselectLabel.setAttribute("id", "multiselect_label_" + timestamp);
        button.setAttribute("id", "multiselect_button_" + timestamp);
        button.setAttribute("type", "button");
        list.setAttribute("id", "multiselect_list_" + timestamp);

        var _fnIsChild = function (element, parent) {
          var node = element.parentNode;
          while (node) {
            if (node === parent) {
              return true;
            }
            node = node.parentNode;
          }
          return false;
        };

        var _selectionText = function (element) {
          var text = "";
          var selection = element.querySelectorAll("input:checked");
          if (selection.length === 0) {
            text = labels.emptyText;
          } else if (selection.length > 10) {
            text = selection.length + " " + labels.selectedText;
          } else {
            var arr = [];
            for (var i = 0; i < selection.length; i++) {
              arr.push(selection[i].parentNode.textContent);
            }
            text = arr.join(",");
          }

          return text;
        };

        var _openList = function (e) {
          list.style.display = "block";
          e.srcElement.children[0].focus();
        };

        var _selectItem = function () {
          var text = _selectionText(container);
          container
            .getElementsByTagName("button")[0]
            .children[0].setAttribute("placeholder", text);

          if (selectCb) {
            var selectionElements = container.querySelectorAll("input:checked");
            var selection = [];
            for (var i = 0; i < selectionElements.length; i++) {
              selection.push(selectionElements[i].value);
            }
            selectCb(selection);
          }
        };

        var _clearSearch = function () {
          var elements = container.getElementsByTagName("li");
          for (var i = 0; i < elements.length; i++) {
            elements[i].style.display = "";
          }
        };

        var _performSearch = function (e) {
          if (e.which != 13 && e.which != 38 && e.which != 40) {
            var active = list.getElementsByClassName("multiselect-label--active");
            if (active.length > 0) {
              active[0].classList.remove("multiselect-label--active");
            }
            var first = true;
            var filter = e.srcElement.value.toUpperCase();
            var elements = container.getElementsByTagName("li");
            for (var i = 0; i < elements.length; i++) {
              var cb = elements[i].getElementsByTagName("label")[0].textContent;
              if (cb.toUpperCase().indexOf(filter) !== -1) {
                if (first) {
                  first = false;
                  elements[i].children[0].children[0].classList.add(
                    "multiselect-label--active"
                  );
                }
                elements[i].style.display = "";
              } else {
                elements[i].style.display = "none";
              }
            }
          }
        };

        var _fnClearSelection = function (e) {
          var inputs = list.getElementsByTagName("input");
          for (var i = 0; i < inputs.length; i++) {
            if (inputs[i].checked) {
              inputs[i].parentNode.click();
            }
          }
          e.stopPropagation();
        };

        var _fnSelectAll = function (e) {
          var inputs = list.getElementsByTagName("input");
          for (var i = 0; i < inputs.length; i++) {
            if (!inputs[i].checked) {
              inputs[i].parentNode.click();
            }
          }
          e.stopPropagation();
        };

        container.classList.add("multiselect-container");
        multiselectLabel.classList.add("multiselect-label");
        dataContainer.classList.add("multiselect-data-container");
        button.classList.add("multiselect-button");

        searchField.setAttribute("type", "text");
        searchField.setAttribute("placeholder", labels.emptyText);
        searchField.classList.add("multiselect-text");
        searchField.addEventListener("keyup", _performSearch);
        searchField.setAttribute("data", JSON.stringify(targetData));

        clearSelection.classList.add("multiselect-clear");
        clearSelection.innerHTML = "X";
        clearSelection.addEventListener("click", _fnClearSelection);

        carret.classList.add("carret");

        button.appendChild(searchField);
        button.appendChild(clearSelection);
        button.appendChild(carret);

        button.addEventListener("click", _openList);

        list.classList.add("multiselect-list");

        for (var i = -1; i < data.length; i++) {
          var item = document.createElement("li");
          var a = document.createElement("a");
          var label = document.createElement("label");
          var input = document.createElement("input");

          a.setAttribute("tabindex", "0");

          label.classList.add("multiselect-item-label");

          if (i == -1) {
            a.addEventListener("click", _fnSelectAll);
            label.appendChild(document.createTextNode("Select all"));
            label.classList.add("multiselect-item-label--select-all");
          } else {
            if (i == 0) {
              label.classList.add("multiselect-item-label--active");
            }
            input.setAttribute("type", "checkbox");
            input.setAttribute("class", "multiselect-checkbox");
            label.appendChild(input);
            input.setAttribute("value", data[i].value);
            input.addEventListener("change", _selectItem);
            label.appendChild(document.createTextNode(data[i].label));
          }
          a.appendChild(label);
          item.appendChild(a);
          list.appendChild(item);
        }

        dataContainer.appendChild(labelElement);
        dataContainer.appendChild(multiselectbefore);
        dataContainer.appendChild(button);
        dataContainer.appendChild(list);
        dataContainer.appendChild(multiselectdesc);
        dataContainer.appendChild(multiselectbetween);
        dataContainer.appendChild(multiselectafter);
        container.appendChild(multiselectLabel);
        container.appendChild(dataContainer);

        //Change to the specific window
        document.addEventListener("click", function (e) {
          if (!_fnIsChild(e.target, container)) {
            list.style.display = "none";
            searchField.value = "";
            _clearSearch();
          }
        });

        document.addEventListener("keyup", function (e) {
          if (list.style.display == "block") {
            //mouse down
            if (e.which === 40) {
              var active = list.getElementsByClassName("multiselect-label--active")[0];
              var next = active.parentNode.parentNode.nextSibling;
              //Find the next visible element
              while (next && next.style && next.style.display == "none") {
                next = next.nextSibling;
              }
              if (next) {
                active.classList.remove("multiselect-label--active");
                next
                  .getElementsByClassName("multiselect-label")[0]
                  .classList.add("multiselect-label--active");
                next.children[0].focus();
                searchField.focus();
                e.preventDefault();
              }
            } else if (e.which === 38) {
              //mouse up
              var active1 = list.getElementsByClassName("multiselect-label--active")[0];
              var prev = active1.parentNode.parentNode.previousSibling;
              //Find the previous visible element
              while (prev && prev.style && prev.style.display === "none") {
                prev = prev.previousSibling;
              }
              if (prev) {
                active1.classList.remove("multiselect-label--active");
                prev
                  .getElementsByClassName("multiselect-label")[0]
                  .classList.add("multiselect-label--active");
                prev.children[0].focus();
                searchField.focus();
                e.preventDefault();
              }
            } else if (e.which === 13) {
              // enter
              list.getElementsByClassName("multiselect-label--active")[0].click();
              e.preventDefault();
            }
          }
        });
      };
      var exportObj = {
        init: function (element, data, selectCb, options) {
          createMultiselect(element, data, selectCb, options);
        },
      };

      Motus.ElementMultiselect = exportObj;
      var data = [];
      var element = document.getElementById("multiselect__container");
      var element2 = document.getElementById("multiselect__container2");

      var select = function (data) {
        console.log(data);
      };

      Motus.ElementMultiselect.init(element, data, select);
      Motus.ElementMultiselect.init(element2, data, select);
      // Append the label and multiple select field to the drop-container
      const dropContainer = document.getElementById("drop-container");
      // containerSelectDiv.appendChild(label);
      // containerSelectDiv.appendChild(multipleSelectField);
      // Append the container div to the drop-container
      console.log(container);
      var ssMainContainer = document.createElement("div");

      ssMainContainer.className =
        "position-absolute justify-content-between w-100 vfb-action";

      ssMainContainer.identification = "mainContainer_" + this.imageCount;

      var ssNameTagDiv = document.createElement("div");
      ssNameTagDiv.className = "vfb-preview-element-name-tag-div";

      var ssNameLabel = document.createElement("div");
      ssNameLabel.className = "vfb-preview-element-name-tag";
      ssNameLabel.textContent = "text";

      // Set identification property for ssNameLabel
      ssNameLabel.identification = "nameLabel_" + this.imageCount;

      ssNameTagDiv.appendChild(ssNameLabel);

      // Create the second child
      var ssActionsContainer = document.createElement("div");
      ssActionsContainer.className = "vfb-preview-element-actions-container";

      var ssCloneDiv = document.createElement("div");
      ssCloneDiv.className = "vfb-clone";

      ssCloneDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zM362 464H54a6 6 0 0 1-6-6V150a6 6 0 0 1 6-6h42v224c0 26.51 21.49 48 48 48h224v42a6 6 0 0 1-6 6zm96-96H150a6 6 0 0 1-6-6V54a6 6 0 0 1 6-6h308a6 6 0 0 1 6 6v308a6 6 0 0 1-6 6z"></path></svg>
`;

      var ssDeleteDiv = document.createElement("div");
      ssDeleteDiv.className = "vfb-delete";

      ssDeleteDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M268 416h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12zM432 80h-82.41l-34-56.7A48 48 0 0 0 274.41 0H173.59a48 48 0 0 0-41.16 23.3L98.41 80H16A16 16 0 0 0 0 96v16a16 16 0 0 0 16 16h16v336a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V128h16a16 16 0 0 0 16-16V96a16 16 0 0 0-16-16zM171.84 50.91A6 6 0 0 1 177 48h94a6 6 0 0 1 5.15 2.91L293.61 80H154.39zM368 464H80V128h288zm-212-48h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12z"></path></svg>
`;
      ssActionsContainer.appendChild(ssCloneDiv);
      ssCloneDiv.onclick = this.cloneSelectElement;
      ssActionsContainer.appendChild(ssDeleteDiv);
      ssDeleteDiv.onclick = this.deleteElement;
      // Append children to the main container
      ssMainContainer.appendChild(ssNameTagDiv);
      ssMainContainer.appendChild(ssActionsContainer);

      // Append the main container to another container (e.g., containerTextDiv)
      container.appendChild(ssMainContainer);

      container.addEventListener("click", this.handleSelect);
      if (this.currentTabID != "") {
        document.getElementById(this.currentTabID).appendChild(container);
      } else {
        dropContainer.appendChild(container);
      }
      // Hide the remv-after-dropped section
      const remvAfterDropped = document.getElementById("remv-after-dropped");
      remvAfterDropped.style.display = "none";
    },
    appendImageElement(targetData, clone) {
      const dropContainer = document.getElementById("drop-container");
      const containerImageUploadDiv = document.createElement("div");
      containerImageUploadDiv.classList.add(
        "containerImageUploadDiv",
        "font-default",
        "box"
      );
      containerImageUploadDiv.id = "containerImageUploadDiv";
      containerImageUploadDiv.onclick = this.handleImage;
      containerImageUploadDiv.draggable = true;
      const ImageUploadField = document.createElement("img");
      const anchorField = document.createElement("a");
      const staticImgDiv = document.createElement("div");
      staticImgDiv.classList.add("form-static-tag-img", "text-start", "mt-0", "mb-0");
      staticImgDiv.setAttribute("data-alignment", "text-start");
      staticImgDiv.setAttribute("space-top", "mt-0");
      staticImgDiv.setAttribute("space-bottom", "mb-0");

      ImageUploadField.src = "https://vueform.com/images/logo.svg"; // Replace with the actual URL of your image
      ImageUploadField.alt = "Image not found"; // Provide alternative text for accessibility
      ImageUploadField.classList.add("imge-container"); // Add any custom classes you need
      // console.log(htmlAppend);
      this.imageCount++;
      ImageUploadField.setAttribute("data", JSON.stringify(targetData));

      // containerUploadDiv.onclick = this.handleMultiImage;
      var label = document.createElement("label");

      containerImageUploadDiv.appendChild(label);
      anchorField.appendChild(ImageUploadField);
      staticImgDiv.appendChild(anchorField);
      containerImageUploadDiv.appendChild(staticImgDiv);
      var hoverableUploaddiv = document.createElement("div");
      hoverableUploaddiv.classList.add("hoverableUpload");
      // hoverableUploaddiv.innerHTML = htmlAppend; // Use 'innerHTML' with a capital 'I'
      containerImageUploadDiv.appendChild(hoverableUploaddiv);
      var newUploadDivBefore = document.createElement("div");
      newUploadDivBefore.classList.add("vfb-preview-element-main-wrapper-before-Upload");
      var newUploadDivBetween = document.createElement("div");
      newUploadDivBetween.classList.add(
        "vfb-preview-element-main-wrapper-between-Upload"
      );
      var newUploadDivDesc = document.createElement("div");
      newUploadDivDesc.classList.add("vfb-preview-element-main-wrapper-desc-Upload");
      var newUploadDivAfter = document.createElement("div");
      newUploadDivAfter.classList.add("vfb-preview-element-main-wrapper-after-Upload");
      var newUploadDivSpan = document.createElement("span");
      newUploadDivSpan.classList.add("vfb-preview-element-Upload-Autofloat");
      var ImgMainContainer = document.createElement("div");
      // ImgMainContainer.onclick = this.handleInput;
      ImgMainContainer.className =
        "position-absolute justify-content-between w-100 vfb-action";

      // Set identification property for ImgMainContainer
      ImgMainContainer.identification = "mainContainer_" + this.imageCount;

      // Create the first child
      var ImgNameTagDiv = document.createElement("div");
      ImgNameTagDiv.className = "vfb-preview-element-name-tag-div";

      var ImgNameLabel = document.createElement("div");
      ImgNameLabel.className = "vfb-preview-element-name-tag";
      ImgNameLabel.textContent = "text";

      // Set identification property for ImgNameLabel
      ImgNameLabel.identification = "nameLabel_" + this.imageCount;

      ImgNameTagDiv.appendChild(ImgNameLabel);

      // Create the second child
      var ImgActionsContainer = document.createElement("div");
      ImgActionsContainer.className = "vfb-preview-element-actions-container";

      var ImgCloneDiv = document.createElement("div");
      ImgCloneDiv.className = "vfb-clone";

      ImgCloneDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zM362 464H54a6 6 0 0 1-6-6V150a6 6 0 0 1 6-6h42v224c0 26.51 21.49 48 48 48h224v42a6 6 0 0 1-6 6zm96-96H150a6 6 0 0 1-6-6V54a6 6 0 0 1 6-6h308a6 6 0 0 1 6 6v308a6 6 0 0 1-6 6z"></path></svg>
`;

      var ImgDeleteDiv = document.createElement("div");
      ImgDeleteDiv.className = "vfb-delete";

      ImgDeleteDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M268 416h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12zM432 80h-82.41l-34-56.7A48 48 0 0 0 274.41 0H173.59a48 48 0 0 0-41.16 23.3L98.41 80H16A16 16 0 0 0 0 96v16a16 16 0 0 0 16 16h16v336a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V128h16a16 16 0 0 0 16-16V96a16 16 0 0 0-16-16zM171.84 50.91A6 6 0 0 1 177 48h94a6 6 0 0 1 5.15 2.91L293.61 80H154.39zM368 464H80V128h288zm-212-48h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12z"></path></svg>
`;

      ImgActionsContainer.appendChild(ImgCloneDiv);
      ImgCloneDiv.onclick = this.cloneImageElement;
      ImgActionsContainer.appendChild(ImgDeleteDiv);
      ImgDeleteDiv.onclick = this.deleteElement;
      // Append children to the main container
      ImgMainContainer.appendChild(ImgNameTagDiv);
      ImgMainContainer.appendChild(ImgActionsContainer);

      // Append the main container to another container (e.g., containerTextDiv)
      containerImageUploadDiv.appendChild(ImgMainContainer);

      // newUploadDivSpan.innerHTML= "spna"
      containerImageUploadDiv.insertBefore(
        newUploadDivBefore,
        containerImageUploadDiv.childNodes[1]
      );
      containerImageUploadDiv.insertBefore(
        newUploadDivSpan,
        containerImageUploadDiv.childNodes[2]
      );
      containerImageUploadDiv.appendChild(newUploadDivBetween);
      containerImageUploadDiv.appendChild(newUploadDivDesc);
      containerImageUploadDiv.appendChild(newUploadDivAfter);

      if (this.currentTabID != "") {
        document.getElementById(this.currentTabID).appendChild(containerImageUploadDiv);
      } else {
        dropContainer.appendChild(containerImageUploadDiv);
      }

      const remvAfterDropped = document.getElementById("remv-after-dropped");
      remvAfterDropped.style.display = "none";
    },
    appendMultiFileElement(targetData, clone) {
    // Array to store imageUrl values
      const dropContainer = document.getElementById("drop-container");
      var containerUploadDiv = document.createElement("div");
      containerUploadDiv.draggable = true;
      // var targetElementData=this.targetElementData;
     

      containerUploadDiv = document.createElement("div");
      containerUploadDiv.classList.add(
        "containerUploadDiv",
        "font-default",
        "col-lg-12",
        "box"
      );
      containerUploadDiv.id = "containerUploadDiv";
      containerUploadDiv.draggable = true;
      // containerUploadDiv.onclick = this.handleMultiImage;
      // console.log(htmlAppend);
      const label = document.createElement("label");
      label.classList.add("col-lg-12");
      label.innerText = "Multi-image";
      const multipleUploadField = document.createElement("input");
      multipleUploadField.classList.add("col-lg-12", "form-input");
      // multipleUploadField.onfocus = this.handleMultiImage;
      multipleUploadField.type = "file";
      multipleUploadField.classList.add("choose-btn");
      multipleUploadField.multiple = true;
      multipleUploadField.setAttribute("data", JSON.stringify(targetData));
      multipleUploadField.identification = "multiimage_" + this.multiImageCount;
      multipleUploadField.id = "multiimage_" + this.multiImageCount;
      // Handle file selection
      // multipleUploadField.addEventListener("change", function () {
      //   handleFileUpload(this.files,targetData);
      // });
      multipleUploadField.onchange = function(event) {
        this.handleFileUpload(event);
}.bind(this);

      // containerUploadDiv.onclick = function () {
      //   document.getElementById("rightMenuMultiImage").style.right = "0px";
      //   document.getElementById("rightMenu").style.right = "-500px";
      //   document.getElementById("multiSelectrightMenu").style.right = "-500px";
      //   this.handleMultiImage;
      //   console.log("clicked");
      // };

      // Create the main container
      var mlMainContainer = document.createElement("div");
      mlMainContainer.onclick = this.handleInput;
      mlMainContainer.className =
        "position-absolute justify-content-between w-100 vfb-action";

      // Set identification property for mlMainContainer
      // mlMainContainer.identification = "mainContainer_" + this.elementCount;

      // Create the first child
      var mlNameTagDiv = document.createElement("div");
      mlNameTagDiv.className = "vfb-preview-element-name-tag-div";

      var mlNameLabel = document.createElement("div");
      mlNameLabel.className = "vfb-preview-element-name-tag";
      mlNameLabel.textContent = "text";

      // Set identification property for mlNameLabel
      // mlNameLabel.identification = "nameLabel_" + this.elementCount;

      mlNameTagDiv.appendChild(mlNameLabel);

      // Create the second child
      var mlActionsContainer = document.createElement("div");
      mlActionsContainer.className = "vfb-preview-element-actions-container";

      var mlCloneDiv = document.createElement("div");
      mlCloneDiv.className = "vfb-clone";

      mlCloneDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zM362 464H54a6 6 0 0 1-6-6V150a6 6 0 0 1 6-6h42v224c0 26.51 21.49 48 48 48h224v42a6 6 0 0 1-6 6zm96-96H150a6 6 0 0 1-6-6V54a6 6 0 0 1 6-6h308a6 6 0 0 1 6 6v308a6 6 0 0 1-6 6z"></path></svg>
`;

      var mlDeleteDiv = document.createElement("div");
      mlDeleteDiv.className = "vfb-delete";

      mlDeleteDiv.innerHTML = `
<svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M268 416h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12zM432 80h-82.41l-34-56.7A48 48 0 0 0 274.41 0H173.59a48 48 0 0 0-41.16 23.3L98.41 80H16A16 16 0 0 0 0 96v16a16 16 0 0 0 16 16h16v336a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V128h16a16 16 0 0 0 16-16V96a16 16 0 0 0-16-16zM171.84 50.91A6 6 0 0 1 177 48h94a6 6 0 0 1 5.15 2.91L293.61 80H154.39zM368 464H80V128h288zm-212-48h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12z"></path></svg>
`;

      mlActionsContainer.appendChild(mlCloneDiv);
      mlActionsContainer.appendChild(mlDeleteDiv);
      mlDeleteDiv.onclick = this.deleteElement;
      mlCloneDiv.onclick = this.cloneMultiFileElement;
      // Append children to the main container
      mlMainContainer.appendChild(mlNameTagDiv);
      mlMainContainer.appendChild(mlActionsContainer);

      // Append the main container to another container (e.g., containerTextDiv)
      containerUploadDiv.appendChild(mlMainContainer);

      containerUploadDiv.onclick = this.handleMultiImage;

      containerUploadDiv.appendChild(label);
      // const lineBreak = document.createElement("br");
      // containerUploadDiv.appendChild(lineBreak);
      containerUploadDiv.appendChild(multipleUploadField);
      var hoverableUploaddiv = document.createElement("div");
      hoverableUploaddiv.classList.add("hoverableUpload");
      // hoverableUploaddiv.innerHTML = htmlAppend;
      containerUploadDiv.appendChild(hoverableUploaddiv);
      // hoverableUploaddiv.querySelector(".vfb-preview-element-name-tag").innerText =
      //   "multiimage_" + this.elementCount;
      var newUploadDivBefore = document.createElement("div");
      newUploadDivBefore.classList.add("vfb-preview-element-main-wrapper-before-Upload");
      var newUploadDivBetween = document.createElement("div");
      newUploadDivBetween.classList.add(
        "vfb-preview-element-main-wrapper-between-Upload"
      );
      var newUploadDivSdesc = document.createElement("div");
      newUploadDivSdesc.classList.add("vfb-preview-element-main-wrapper-desc-Upload");
      var newUploadDivAfter = document.createElement("div");
      newUploadDivAfter.classList.add("vfb-preview-element-main-wrapper-after-Upload");
      var newUploadDivSpan = document.createElement("span");
      newUploadDivSpan.classList.add("vfb-preview-element-Upload-Autofloat");
      // newUploadDivSpan.innerHTML= "spna"
      containerUploadDiv.insertBefore(
        newUploadDivBefore,
        containerUploadDiv.childNodes[1]
      );
      containerUploadDiv.insertBefore(newUploadDivSpan, containerUploadDiv.childNodes[2]);
      containerUploadDiv.appendChild(newUploadDivBetween);
      containerUploadDiv.appendChild(newUploadDivSdesc);
      containerUploadDiv.appendChild(newUploadDivAfter);
      if (this.currentTabID != "") {
        document.getElementById(this.currentTabID).appendChild(containerUploadDiv);
      } else {
        dropContainer.appendChild(containerUploadDiv);
      }

      const remvAfterDropped = document.getElementById("remv-after-dropped");
      remvAfterDropped.style.display = "none";
    },
    appendInputElement(data, clone) {
      let dropContainer = document.getElementById("drop-container");
      const containerTextRow = document.createElement("div");
      containerTextRow.classList.add("row");
      const containerTextDivMain = document.createElement("div");
      containerTextDivMain.classList.add("col-lg-12");
      // Create a new div element to encapsulate the label and text input
      const containerTextDiv = document.createElement("div");

      // Add the CSS class for hover effect
      containerTextDiv.classList.add("container-text-div", "col-lg-12", "font-default");
      containerTextDiv.onclick = this.handleInput;
      // Create a new label element
      const label = document.createElement("label");
      label.innerText = clone ? (data.label != undefined ? data.label : "Text") : "Text";
      label.classList.add("col-lg-12");
      const containerInputDivMain = document.createElement("div");
      containerInputDivMain.classList.add("form-input-Main");
      const containerInputDivSpan = document.createElement("span");
      containerInputDivSpan.classList.add("vfb-floating-span");
      const containerInputDiv = document.createElement("div");
      containerInputDiv.classList.add("form-input", "col-lg-12");

      const vfbwrapper = document.createElement("div");
      vfbwrapper.classList.add("vfb-preview-element-inner-wrapper-before");
      const vfbwrapperafter = document.createElement("div");
      vfbwrapperafter.classList.add("vfb-preview-element-inner-wrapper-after");
      var container;
      // Create a new text field element
      const textField = document.createElement("input");
      // textField.onclick = this.handleInput;
      textField.onfocus = this.handleInput;
      textField.oninput = function (event) {
        this.setElementAttribute(event, "value");
      }.bind(this);
      // textField.onblur = this.handleInput;
      textField.type = "text";
      textField.setAttribute("data", JSON.stringify(data));

      textField.identification = "text_" + this.elementCount;
      textField.classList.add("h-100", "border-0", "rounded");
      containerInputDiv.classList.add("border", "rounded");
      containerInputDiv.style.borderColor = "#d1d5db";

      containerInputDiv.classList.add(
        "w-100",
        "d-flex",
        "align-items-center",
        "px-2",
        "py-2"
      );
      // containerInputDiv.style.height = "40px"; // Remaining custom style for height

      containerTextDiv.onclick = function () {
        // Your onclick logic here
        document.getElementById("rightMenu").style.right = "0px";
        document.getElementById("rightMenuTab").style.right = "-500px";

        document.getElementById("rightMenuMultiImage").style.right = "-500px";
        document.getElementById("multiSelectrightMenu").style.right = "-500px";
        document.getElementById("rightMenuImage").style.right = "-500px";
      };
      // Create the main container
      var vfbFieldsOption = document.createElement("div");
      vfbFieldsOption.classList.add("vfb-fields-option");
      vfbFieldsOption.classList.add("d-none");

      // Create the label element
      var labelContainer = document.createElement("label");
      labelContainer.classList.add("vfb-fields-label");
      labelContainer.textContent = "Text";
      // labelContainer.classList.add("mb-2");
      // Create the container for action buttons
      var actionButtons = document.createElement("div");
      actionButtons.classList.add("vfb-action-buttons");
      var hoverDiv = document.createElement("div");
      hoverDiv.classList.add("hoverable");

      containerTextDiv.appendChild(label);
      var newDivBefore = document.createElement("div");
      var newDivafter = document.createElement("div");
      var newDivbetween = document.createElement("div");
      newDivBefore.classList.add("vfb-preview-element-main-wrapper-before");
      newDivbetween.classList.add("vfb-preview-element-main-wrapper-between");
      newDivafter.classList.add("vfb-preview-element-main-wrapper-after");
      containerTextDiv.appendChild(newDivBefore);

      //drage here functionality here

      var vfbPreviewElementAreaTop = document.createElement("div");
      vfbPreviewElementAreaTop.classList.add("vfbPreviewElementAreaTop");

      var vfbPreviewElementDragLabelWrapper = document.createElement("div");
      vfbPreviewElementDragLabelWrapper.classList.add(
        "vfb-preview-element-drag-label-wrapper"
      );
      vfbPreviewElementAreaTop.append(vfbPreviewElementDragLabelWrapper);

      var vfbPreviewElementDragLabel = document.createElement("label");
      vfbPreviewElementDragLabel.classList.add("vfb-preview-element-drag-label");
      vfbPreviewElementDragLabel.textContent = "Drag it here";

      vfbPreviewElementDragLabelWrapper.append(vfbPreviewElementDragLabel);
      containerTextDiv.insertBefore(
        vfbPreviewElementAreaTop,
        containerTextDiv.firstChild
      );

      var vfbPreviewElementAreaBottom = document.createElement("div");
      vfbPreviewElementAreaBottom.classList.add("vfbPreviewElementAreaBottom");
      containerTextDiv.appendChild(vfbPreviewElementAreaBottom);
      containerTextDiv.addEventListener("dragenter", (event) => {
        vfbPreviewElementAreaTop.style.display = "block";
      });
      containerTextDiv.addEventListener("dragleave", () => {
        // Hide the vfbPreviewElementDragLabelWrapper when the mouse leaves the area
        vfbPreviewElementAreaTop.style.display = "none";
      });
      // Create the main container
      var ttMainContainer = document.createElement("div");
      ttMainContainer.onclick = this.handleInput;
      ttMainContainer.className =
        "position-absolute justify-content-between w-100 vfb-action";

      // Set identification property for ttMainContainer
      ttMainContainer.identification = "mainContainer_" + this.elementCount;

      // Create the first child
      var ttNameTagDiv = document.createElement("div");
      ttNameTagDiv.className = "vfb-preview-element-name-tag-div";

      var ttNameLabel = document.createElement("div");
      ttNameLabel.className = "vfb-preview-element-name-tag";
      ttNameLabel.textContent = "text";

      // Set identification property for ttNameLabel
      ttNameLabel.identification = "nameLabel_" + this.elementCount;

      ttNameTagDiv.appendChild(ttNameLabel);

      // Create the second child
      var ttActionsContainer = document.createElement("div");
      ttActionsContainer.className = "vfb-preview-element-actions-container";

      var ttCloneDiv = document.createElement("div");
      ttCloneDiv.className = "vfb-clone";

      ttCloneDiv.innerHTML = `
    <svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M464 0H144c-26.51 0-48 21.49-48 48v48H48c-26.51 0-48 21.49-48 48v320c0 26.51 21.49 48 48 48h320c26.51 0 48-21.49 48-48v-48h48c26.51 0 48-21.49 48-48V48c0-26.51-21.49-48-48-48zM362 464H54a6 6 0 0 1-6-6V150a6 6 0 0 1 6-6h42v224c0 26.51 21.49 48 48 48h224v42a6 6 0 0 1-6 6zm96-96H150a6 6 0 0 1-6-6V54a6 6 0 0 1 6-6h308a6 6 0 0 1 6 6v308a6 6 0 0 1-6 6z"></path></svg>
`;

      var ttDeleteDiv = document.createElement("div");
      ttDeleteDiv.className = "vfb-delete";

      ttDeleteDiv.innerHTML = `
    <svg class="vfb-icon" aria-hidden="true" focusable="false" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="currentColor" d="M268 416h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12zM432 80h-82.41l-34-56.7A48 48 0 0 0 274.41 0H173.59a48 48 0 0 0-41.16 23.3L98.41 80H16A16 16 0 0 0 0 96v16a16 16 0 0 0 16 16h16v336a48 48 0 0 0 48 48h288a48 48 0 0 0 48-48V128h16a16 16 0 0 0 16-16V96a16 16 0 0 0-16-16zM171.84 50.91A6 6 0 0 1 177 48h94a6 6 0 0 1 5.15 2.91L293.61 80H154.39zM368 464H80V128h288zm-212-48h24a12 12 0 0 0 12-12V188a12 12 0 0 0-12-12h-24a12 12 0 0 0-12 12v216a12 12 0 0 0 12 12z"></path></svg>
`;

      ttActionsContainer.appendChild(ttCloneDiv);
      ttActionsContainer.appendChild(ttDeleteDiv);
      ttDeleteDiv.onclick = this.deleteElement;
      ttCloneDiv.onclick = this.cloneInputElement;
      // Append children to the main container
      ttMainContainer.appendChild(ttNameTagDiv);
      ttMainContainer.appendChild(ttActionsContainer);

      // Append the main container to another container (e.g., containerTextDiv)
      containerTextDiv.appendChild(ttMainContainer);

      //  containerInputDivMain.appendChild(containerInputDivSpan);
      containerInputDivMain.appendChild(textField);
      containerInputDivMain.appendChild(containerInputDivSpan);
      containerInputDivMain.style.width = "100%";
      containerInputDiv.appendChild(containerInputDivMain);
      containerInputDiv.prepend(vfbwrapper);
      containerInputDiv.append(vfbwrapperafter);

      // Assuming you already have the vfbFieldsOption and dropContainer elements
      containerTextDiv.appendChild(containerInputDiv);
      containerTextDiv.appendChild(newDivbetween);
      containerTextDiv.appendChild(newDivafter);
      // Assuming you already have the vfbFieldsOption and dropContainer elements

      // Append the container div to the drop-container

      containerTextDivMain.appendChild(containerTextDiv);
      containerTextRow.appendChild(containerTextDivMain);
      if (this.currentTabID != "") {
        document.getElementById(this.currentTabID).appendChild(containerTextDiv);
      } else {
        dropContainer.appendChild(containerTextDiv);
      }

      // Hide the remv-after-dropped section
      const remvAfterDropped = document.getElementById("remv-after-dropped");
      remvAfterDropped.style.display = "none";
    },
    checkedDefaultsColumns(event) {
      if (!event.target.checked == true) {
        event.target.parentNode.parentNode.previousElementSibling.classList.remove(
          "d-none"
        );
      } else {
        event.target.parentNode.parentNode.previousElementSibling.classList.add("d-none");
      }
    },
    createTabContentArea(tabContentContainer, tabIndex) {
      const tabContent = document.createElement("div");
      tabContent.className = "tab-content3";
      tabContent.id = `tab-content-${tabIndex}`;
      tabContent.textContent = `Content for Tab ${tabIndex}`; // Placeholder text
      tabContentContainer.appendChild(tabContent);
    },
    deleteElement(event) {
      if (this.tab) {
        if (typeof this.finalArr === "object" && !Array.isArray(this.finalArr)) {
          let targetKey = this.targetTabKey;
          let targetTabData = this.finalArr.targetKey;
          if (targetTabData == undefined) {
            targetTabData = this.targetTabData;
          }

          const indexToRemove = targetTabData.elements.findIndex(
            (obj) => obj.identification === this.targetElementData.identification
          );
          targetTabData.elements.splice(indexToRemove, 1);
          this.finalArr = {
            ...this.finalArr,
            [this.targetTabKey]: targetTabData,
          };
        }
      } else {
        const indexToRemove = this.finalArr.findIndex(
          (obj) => obj.identification === this.targetElementData.identification
        );
        this.finalArr.splice(indexToRemove, 1);
      }
      this.$refs.finalArrParentElement.innerHTML = `<pre>${JSON.stringify(
        this.finalArr,
        null,
        2
      )}</pre>`;
      // this.targetElementParent.innerHTML = "";
      var parentElement = document.getElementById("drop-container"); // Replace 'parentElementId' with the actual ID of the parent element
      var childElement = this.targetElementParent; // Assuming this.targetElementParent is the child element you want to remove

      if (parentElement && childElement) {
        parentElement.removeChild(childElement);
      }
      document.getElementById("rightMenuMultiImage").style.right = "-500px";
      document.getElementById("rightMenu").style.right = "-500px";
      document.getElementById("multiSelectrightMenu").style.right = "-500px";
      document.getElementById("rightMenuTab").style.right = "-500px";
      document.getElementById("rightMenuImage").style.right = "-500px";
    },
    cloneInputElement(event) {
      this.elementCount++;
      let targetElementData = this.targetElementData;
      let identification = "identification";
      let updatedTargetElementData = {
        ...targetElementData,
        [identification]: "text_" + this.elementCount,
      };
      this.appendInputElement(updatedTargetElementData, true);
    },
    cloneMultiFileElement(event) {
      this.elementCount++;
      let targetElementData = this.targetElementData;
      let identification = "identification";
      let updatedTargetElementData = {
        ...targetElementData,
        [identification]: "multiimage_" + this.elementCount,
      };
      this.appendMultiFileElement(updatedTargetElementData, true);
    },
    cloneImageElement(event) {
      this.elementCount++;
      let targetElementData = this.targetElementData;
      let identification = "identification";
      let updatedTargetElementData = {
        ...targetElementData,
        [identification]: "img_" + this.elementCount,
      };
      this.appendImageElement(updatedTargetElementData, true);
    },
    cloneSelectElement(event) {
      this.elementCount++;
      let targetElementData = this.targetElementData;
      let identification = "identification";
      let updatedTargetElementData = {
        ...targetElementData,
        [identification]: "multiple_select_" + this.elementCount,
      };
      this.appendSelectElement(updatedTargetElementData, true);
    },
    handleDrop(event) {
      // Check if the event has already been handled
      if (event.defaultPrevented) {
        return;
      }
      // console.log("handleDrop")handleIn;

      const dropContainer = document.getElementById("drop-container");
      dropContainer.style.backgroundColor = "";
      event.preventDefault();
      const dataCode = event.dataTransfer.getData("text/plain");

      // ...

      var containerUploadDiv = document.createElement("div");
      function handleFileUpload(files) {
        alert(true)
  const uploadedImageUrls = []; // Array to store imageUrl values

  for (const file of files) {
    const imageUrl = URL.createObjectURL(file);
    uploadedImageUrls.push(imageUrl); // Add imageUrl to the array

    const maindiv = document.createElement("div");
    const imageUrlDiv = document.createElement("div");
    const imageDiv = document.createElement("div");
    const image = document.createElement("img");

    // Adding classes
    maindiv.classList.add("vfb-file-upload", "d-flex");
    imageUrlDiv.classList.add("vfb-file-url");
    image.src = imageUrl;
    imageUrlDiv.innerText = imageUrl;

    imageDiv.appendChild(image);
    maindiv.appendChild(imageDiv);
    maindiv.appendChild(imageUrlDiv);

    // Appending maindiv to dropContainer
    containerUploadDiv.appendChild(maindiv);
  }

  console.log("Uploaded Image URLs:", uploadedImageUrls);
}


      if (dataCode === "Text") {
        this.elementCount++;
        let data = {
          identification: "text_" + this.elementCount,
          fieldType: "TextInput",
          autoFloat: "default",
          customAttributes: [],
          columns: {
            default: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },

            tablet: {
              container: "col-md-12 col-sm-12",
              label: "col-md-12 col-sm-12",
              wrapper: "col-md-12 col-sm-12",
            },
            desktop: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },
          },
        };
        this.appendInputElement(data, false);
      }
      // ...
      else if (dataCode === "multiple_select") {
        var elementCount = ++this.elementCount;
        let data = {
          identification: "multiple_select_" + elementCount,
          fieldType: "multipleSelect",
          autoFloat: "default",
          customAttributes: [],
          options: [],
          columns: {
            default: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },

            tablet: {
              container: "col-md-12 col-sm-12",
              label: "col-md-12 col-sm-12",
              wrapper: "col-md-12 col-sm-12",
            },
            desktop: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },
          },
        };
        this.appendSelectElement(data, false);
      } else if (dataCode === "upload") {
        this.elementCount++;
        let data = {
          identification: "multiimage_" + this.elementCount,
          fieldType: "multiimage",
          autoFloat: "default",
          customAttributes: [],
          columns: {
            default: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },

            tablet: {
              container: "col-md-12 col-sm-12",
              label: "col-md-12 col-sm-12",
              wrapper: "col-md-12 col-sm-12",
            },
            desktop: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },
          },
        };
        this.appendMultiFileElement(data, false);
      } else if (dataCode === "ImageUpload") {
        this.elementCount++;
        let data = {
          identification: "img_" + this.elementCount,
          fieldType: "image",
          autoFloat: "default",
          customAttributes: [],
          columns: {
            default: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },

            tablet: {
              container: "col-md-12 col-sm-12",
              label: "col-md-12 col-sm-12",
              wrapper: "col-md-12 col-sm-12",
            },
            desktop: {
              container: "col-lg-12",
              label: "col-lg-12",
              wrapper: "col-lg-12",
            },
          },
        };
        this.appendImageElement(data, false);
      } else if (dataCode === "VueTabs") {
        this.createNewTab();
        const remvAfterDropped = document.getElementById("remv-after-dropped");
        remvAfterDropped.style.display = "none";
        tabsNameContainer.onclick = function () {
          document.getElementById("rightMenuTab").style.right = "0px";
          document.getElementById("rightMenuImage").style.right = "-500px";
          document.getElementById("rightMenuMultiImage").style.right = "-500px";
          document.getElementById("rightMenu").style.right = "-500px";
          document.getElementById("multiSelectrightMenu").style.right = "-500px";
          console.log("clicked");
        };
      }
    },
    
    //      handleDragAbleStart(e) {
    //   e.dataTransfer.setData("text/plain", e.target.id);
    // },
    //  handleDragAbleOver(e) {
    //   e.preventDefault();
    // },
    //  handleDropAble(e) {
    //   e.preventDefault();
    //   const dropContainer = document.getElementById("drop-container");
    //   const draggedElementId = e.dataTransfer.getData("text/plain");
    //   const targetElement = e.target;

    //   if (targetElement.classList.contains("box")) {
    //     const elements = Array.from(dropContainer.querySelectorAll(".box"));
    //     const draggedElement = document.getElementById(draggedElementId);
    //     const draggedIndex = elements.indexOf(draggedElement);
    //     const targetIndex = elements.indexOf(targetElement);

    //     if (draggedIndex !== -1 && targetIndex !== -1) {
    //       dropContainer.insertBefore(draggedElement, targetElement);
    //     }
    //   }
    // }
  },
  components: {
    sidebar
  },
};
</script>

<style scoped>
#kt_app_content_container,.app-container.container-fluid{
  display:flex !important;
} 
.vfb-right-container {
  position: absolute;
  right: 0;
  z-index: +1;
  background: #fff;
  height: 100%;
}

/* TextField CSS */

.vfb-config-panel-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.vfb-config-panel-header-wrapper-right {
  display: flex;
}

.vfb-config-panel-header-container {
  margin-left: -1.25rem;
  margin-right: -1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom-width: 1px;
  --tw-border-opacity: 1;
  border-color: rgb(226 232 240 / var(--tw-border-opacity));
  --tw-bg-opacity: 1;
  background-color: rgb(241 245 249 / var(--tw-bg-opacity));
  padding: 1rem 1.85rem;
}

.vfb-config-panel-header-close {
  margin-top: 0.125rem;
  margin-right: 0.5rem;
  cursor: pointer;
  --tw-text-opacity: 1;
  color: rgb(148 163 184 / var(--tw-text-opacity));
  transition-property: color, background-color, border-color, text-decoration-color, fill,
    stroke;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-duration: 0.15s;
}

.vfb-config-panel-header-label {
  font-size: 1.375rem;
}

.vfb-config-panel-header-clone {
  font-size: 0.9375rem;
}

.vfb-config-panel-header-clone,
.vfb-config-panel-header-remove {
  margin-right: 0.75rem;
}

.form-bg-primary {
  background-color: #17c495;
  color: white;
  padding: 4px 10px;
  border-radius: 8px;
}

#rightMenu {
  position: fixed;
  top: 5rem;
  /* right: -300px; Start with it hidden off-screen */

  height: 100%;

  transition: right 0.3s ease;
  /* Add a transition effect to the right property */
}

.vfb-right-container {
  position: absolute;
  right: 0;
  z-index: +1;
  background: #fff;
  height: 100%;
}

/* TextField CSS */

.vfb-config-panel-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.vfb-config-panel-header-wrapper-right {
  display: flex;
}

.vfb-config-panel-header-container {
  margin-left: -1.25rem;
  margin-right: -1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom-width: 1px;
  --tw-border-opacity: 1;
  border-color: rgb(226 232 240 / var(--tw-border-opacity));
  --tw-bg-opacity: 1;
  background-color: rgb(241 245 249 / var(--tw-bg-opacity));
  padding: 1rem 1.85rem;
}

.vfb-config-panel-header-close {
  margin-top: 0.125rem;
  margin-right: 0.5rem;
  cursor: pointer;
  --tw-text-opacity: 1;
  color: rgb(148 163 184 / var(--tw-text-opacity));
  transition-property: color, background-color, border-color, text-decoration-color, fill,
    stroke;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-duration: 0.15s;
}

.vfb-config-panel-header-label {
  font-size: 1.375rem;
}

.vfb-config-panel-header-clone {
  font-size: 0.9375rem;
}

.vfb-config-panel-header-clone,
.vfb-config-panel-header-remove {
  margin-right: 0.75rem;
}

.form-bg-primary {
  background-color: #17c495;
  color: white;
  padding: 4px 10px;
  border-radius: 8px;
}

#multiSelectrightMenu {
  position: fixed;
  top: 0px;
  top: 5rem;
  /* right: -300px; Start with it hidden off-screen */

  height: 100%;

  transition: right 0.3s ease;
  /* Add a transition effect to the right property */
}

#rightMenuMultiImage {
  position: fixed;
  top: 0px;
  top: 5rem;
  /* right: -300px; Start with it hidden off-screen */

  height: 100%;

  transition: right 0.3s ease;
  /* Add a transition effect to the right property */
}

#rightMenuImage {
  position: fixed;
  top: 0px;
  top: 5rem;
  /* right: -300px; Start with it hidden off-screen */

  height: 100%;

  transition: right 0.3s ease;
  /* Add a transition effect to the right property */
}

#rightMenuTab {
  position: fixed;
  top: 0px;
  top: 5rem;
  /* right: -300px; Start with it hidden off-screen */

  height: 100%;

  transition: right 0.3s ease;
  /* Add a transition effect to the right property */
}
</style>
