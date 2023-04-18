<template>
  <div id="mainWrapper" class="flex flex-col h-screen w-full bg-gray-200">
    <TopBar></TopBar>

    <div class="flex flex-row items-stretch p-3 gap-3">
      <Sidebar></Sidebar>
      <MainContent></MainContent>
    </div>
  </div>
</template>

<script>
  import TopBar from './components/TopBar.vue';
  import Sidebar from './components/Sidebar.vue';
  import MainContent from './components/MainContent.vue';

  export default {
    components: {
      TopBar, Sidebar, MainContent
    }
  }
</script>
