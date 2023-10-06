<script setup>
import { RouterLink, RouterView } from 'vue-router'
import SkillsView from '@/components/SkillsView.vue';
import ToolsView from '@/components/ToolsView.vue';
import { useRouter } from 'vue-router'
const router = useRouter();
import { defineProps } from 'vue';

let props = defineProps({
  name:{
    type: Boolean,
    required: true, 
    default: true, 
  }
})

const changeActive = () => {
  this.name.$emit = false;
}

</script>

<template>
  <main>
    <div class="about w-4/6 ml-auto mr-auto mt-10 bg-neutral-800 pl-5 pr-4 pt-5 pb-5 rounded-xl">
      <p class="text-white font-bold text-lg pb-4 uppercase pl-4">About me</p><hr class="border-1 border-yellow-300 border">
      <div class="flex text-white items-center justify-around pt-4">
        <img src="@/assets/25.jpg" class="h-[250px] w-[250px] rounded-full">
        <div class="max-w-50 w-1/2 break-words space-y-3 text-md">
          <p class="">
            Hi everyone! My name is Auriel James V. Fernandez from Mangatarem, Pangasinan. Currently I am a software QA Engineer in Makati city.
            While working, I make time to study modern Tech stacks in Web development so that I can handle web application projects in the future.
          </p>
          <p>
              I really enjoy what I do right now. In my opinion, Creating a program is not just a job, but also an art that has aesthetic value.
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
        <button @click="changeActive" class="text-white font-semibold hover:bg-neutral-800 focus:bg-neutral-800 pt-2 hover:rounded-sm focus:rounded-sm pb-2 pr-3 pl-3 focus:text-yellow-300 focus:border-yellow-300 hover:border-yellow-300 animation duration-300">Tech Stack</button>
        <button class="text-white font-semibold hover:bg-neutral-800 focus:bg-neutral-800 pt-2 hover:rounded-sm focus:rounded-sm pb-2 pr-3 pl-3 focus:text-yellow-300 focus:border-yellow-300 hover:border-yellow-300 animation duration-300">Tools</button>
      </div>
      <SkillsView />
      <p class="text-white">active button {{ props.name }}</p>
    </div>
  </main>
</template>
