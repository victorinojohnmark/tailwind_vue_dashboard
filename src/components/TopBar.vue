<template>
  <div class="w-full flex flex-row gap-4 bg-white">
    <div class="basis-2/12 flex">
      <h1 class="text-3xl font-sans font-bold mx-4 self-center text-green-600">BPMS</h1>
    </div>
    <div class="basis-1/2 flex flex-row p-2">
      
      <div class="bg-gray-200 flex flex-row gap-2 items-center content-center w-full rounded-md p-2">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="#155e75" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
        </svg>
        <input type="text" name="search" class="bg-gray-200 !outline-none text-sm w-full" placeholder="...">
      </div>
    </div>

    <div class="basis-4/12 flex flex-row p-2 gap-4 items-center place-content-end">
      
      
      <div class="flex flex-row gap-4">
        <button class="flex flex-row gap-2 py-1 px-2 hover:bg-gray-100 hover:cursor-pointer rounded-md content-center items-center" @click="toggleMenu">
          <span class="text-gray-700 font-bold">John Mark V.</span>
          <img src="../assets/img/image-placeholder.jpg" alt="" class="w-8 h-8 rounded-full">
        </button>
        <!-- <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="gray" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg> -->

        <div ref="topbarMenu" class="absolute z-10 right-2 top-16 w-56 rounded-lg bg-white text-gray-700 overflow-hidden shadow-lg" :class="{hidden: isHiddenTopBar}">
          <ul class="list-none">
            <li>
              <a href="#" class="p-3 bg-white hover:bg-gray-100 flex flex-row gap-2">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="gray" class="w-6 h-6 hover:cursor-pointer">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0" />
                </svg>
                <span>Notification</span>
              </a>
            </li>
            <li>
              <a href="#" class="p-3 bg-white hover:bg-gray-100 flex flex-row gap-2">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="gray" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15M12 9l-3 3m0 0l3 3m-3-3h12.75" />
                </svg>
                <span>Logout</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  let isHiddenTopBar = ref(true);
  const topbarMenu = ref(null)

  const toggleMenu = () => {
    isHiddenTopBar.value = !isHiddenTopBar.value;
    console.log(topbarMenu, isHiddenTopBar)
  }

</script>