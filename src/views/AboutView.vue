<script setup>
import { RouterLink, RouterView } from 'vue-router'
import SkillsView from '@/components/SkillsView.vue';
import ToolsView from '@/components/ToolsView.vue';
import { useRouter } from 'vue-router'
const router = useRouter();
import { defineProps } from 'vue';
import { ref } from 'vue';

var isActive = ref('techstack');

const changeActive = (event) => {
  isActive.value = event.currentTarget.id;
}

</script>

<template>
  <main>
    <div class="about w-4/6 ml-auto mr-auto mt-10 bg-neutral-800 pl-5 pr-4 pt-5 pb-5 rounded-xl">
      <p class="text-white font-bold text-lg pb-4 uppercase pl-4">About me</p><hr class="border-1 border-yellow-300 border">
      <div class="flex text-white items-center justify-around pt-4">
        <img src="@/assets/25.jpg" class="h-[250px] w-[250px] rounded-full">
        <div class="max-w-50 w-1/2 break-words space-y-3 text-md">
         <p>
         "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
         </p>
        </div>
      </div>
    </div>
    <div class="w-4/6 ml-auto mr-auto">
      <div class="flex pt-10 font-semibold items-center">
        <hr class="border border-1 border-yellow-300 w-20">
        <p class="text-white pl-3 text-xl">Skills</p>
      </div>
      <div class="space-x-2 pt-3">
        <button v-if="isActive==='techstack'" v-on:click="changeActive($event)" id="techstack" class="text-white font-semibold bg-neutral-800 pt-2  rounded-sm pb-2 pr-3 pl-3 text-yellow-300 border-yellow-300 animation duration-300">Tech Stack
        </button>
        <button v-else id="techstack" v-on:click="changeActive($event)" class="text-white font-semibold hover:bg-neutral-800  pt-2 hover:rounded-sm  pb-2 pr-3 pl-3 hover:border-yellow-300 animation duration-300">Tech Stack
        </button>
        <button v-if="isActive==='tools'" v-on:click="changeActive($event)" id="tools" class="text-white font-semibold bg-neutral-800 pt-2  rounded-sm pb-2 pr-3 pl-3 text-yellow-300 border-yellow-300 animation duration-300">Tools
        </button>
        <button v-else id="tools" v-on:click="changeActive($event)" class="text-white font-semibold hover:bg-neutral-800  pt-2 hover:rounded-sm  pb-2 pr-3 pl-3 hover:border-yellow-300 animation duration-300">Tools
        </button>
      </div>
      <div v-if="isActive === 'techstack'" class="animation transition transition-opacity duration-300 ">
        <SkillsView />
      </div>
      <div v-else class="animation duration-300">
        <ToolsView />
      </div>
    </div>
  </main>
</template>
