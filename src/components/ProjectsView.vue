<script setup>

const projects = [
    {
        title: 'Personal Website',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        img: 'src/assets/portfolio.png',
        language: 'VueJS 3, Tailwind',
        role: 'Author',
        link: 'https://github.com/chaesthetics/Portfolio',
    },
    {
        title: 'Instagram Clone',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        img: 'src/assets/instagram.png',
        language: 'Blade, Laravel 10, Tailwind',
        role: 'Author',
        link: 'https://github.com/chaesthetics/Portfolio',
    },
    {
        title: 'CRM',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        img: 'src/assets/crm.png',
        language: 'NextJS, Laravel, Tailwind',
        role: 'Collaborator',
        link: 'https://github.com/chaesthetics/Portfolio',
    },
    {
        title: 'Weather App',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        img: 'src/assets/weatherapp.png',
        language: 'ReactJs, ApiFetch, Tailwind',
        role: 'Author',
        link: 'https://github.com/chaesthetics/Portfolio',
    },
    {
        title: 'Twitter Clone',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        img: 'src/assets/twitter.png',
        language: 'Php, Tailwind',
        role: 'Collaborator',
        link: 'https://github.com/chaesthetics/Portfolio',
    },
    {
        title: 'Anime list',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        img: 'src/assets/animelist.png',
        language: 'ReactJs, ApiFetch, Bootstrap5',
        role: 'Author',
        link: 'https://github.com/chaesthetics/Portfolio',
    },
];

</script>
<template>
<div class="grid grid-cols-3 gap-4 mt-10 pb-10 text-white">
    <div v-for="project in projects" :key="project.title" class="bg-neutral-800 rounded-xl hover:bg-neutral-700 hover:-translate-y-1 hover:scale-110 animation duration-300">
        <div class="pt-5 pb-5 pr-5 pl-5">
            <div class="space-y-2">
                <img :src="project.img" class="rounded-md">
                <p class="text-white font-bold text-md text-center">{{ project.title }}</p>
                <p class="text-white text-sm text-left">{{ project.description }}</p>
            </div>
            <div class="pt-5">
                <p class="text-yellow-300 text-sm font-semibold">{{ project.language }}</p>
                <div class="flex justify-between items-center">
                    <p class="text-xs">-{{ project.role }}</p>
                    <div class="flex  space-x-2">
                        <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" fill="currentColor" class="bi bi-github text-white" viewBox="0 0 16 16"> <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/> </svg>
                        <svg style="color: white" xmlns="http://www.w3.org/2000/svg" width="15" height="15" fill="currentColor" class="bi bi-box-arrow-in-up-right" viewBox="0 0 16 16"> <path fill-rule="evenodd" d="M6.364 13.5a.5.5 0 0 0 .5.5H13.5a1.5 1.5 0 0 0 1.5-1.5v-10A1.5 1.5 0 0 0 13.5 1h-10A1.5 1.5 0 0 0 2 2.5v6.636a.5.5 0 1 0 1 0V2.5a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 .5.5v10a.5.5 0 0 1-.5.5H6.864a.5.5 0 0 0-.5.5z" fill="white"></path> <path fill-rule="evenodd" d="M11 5.5a.5.5 0 0 0-.5-.5h-5a.5.5 0 0 0 0 1h3.793l-8.147 8.146a.5.5 0 0 0 .708.708L10 6.707V10.5a.5.5 0 0 0 1 0v-5z" fill="white"></path> </svg>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>