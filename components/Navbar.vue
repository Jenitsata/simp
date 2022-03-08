<template>
  <div>
    <body class="flex space-x-0 fixed">
      <div
        class="flex flex-col items-center h-screen fixed overflow-hidden text-gray-800 bg-yellow-100 rounded hover:shadow-xl"
      >
        <a class="flex flex-inline items-center w-full px-3 mt-3" href="/">
          <img src="~/assets/mushroom.png" alt="" class="w-10" />
          <span class="ml-2 text-sm font-bold">เห็ดลม</span>
        </a>
        <div class="w-full px-2">
          <div
            class="flex flex-col items-center w-full mt-2 border-t border-gray-700"
          >
            <a
              class="flex items-center w-full h-12 px-3 mt-2 rounded text-gray-800 hover:bg-red-300 text-white"
              href="/simp"
            >
              <svg
                class="h-5 w-5"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <polyline points="22 12 16 12 14 15 10 15 8 12 2 12"></polyline>
                <path
                  d="M5.45 5.11L2 12v6a2 2 0 0 0 2 2h16a2 2 0 0 0
							2-2v-6l-3.45-6.89A2 2 0 0 0 16.76 4H7.24a2 2 0 0
							0-1.79 1.11z"
                ></path>
              </svg>
              <span class="ml-2 text-sm font-medium">Products</span>
            </a>
          </div>
        </div>
        <a
          class="flex items-center justify-center w-full h-16 mt-auto bg-yellow-100 text-gray-800 hover:bg-red-300 text-white"
          href="/simp/profile/"
        >
          <svg
            class="w-6 h-6 stroke-current"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M5.121 17.804A13.937 13.937 0 0112 16c2.5 0 4.847.655 6.879 1.804M15 10a3 3 0 11-6 0 3 3 0 016 0zm6 2a9 9 0 11-18 0 9 9 0 0118 0z"
            />
          </svg>
          <span class="ml-2 text-sm font-medium">Profile</span>
        </a>
      </div>
    </body>
  </div>
</template>

<script>
import products from "~/pages/index";
export default {};
</script>

<style>
.checkout-box {
    width: 100%;
    max-width: 900px;
    display: flex;
    flex-direction: column;
    margin: 50px auto;
    box-sizing: border-box;
    padding: 1em;
  }
  
</style>
