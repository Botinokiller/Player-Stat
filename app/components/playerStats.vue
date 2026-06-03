<template>
    <div class="w-full h-screen flex flex-col gap-5 justify-center items-center bg-yellow-500 bg-opacity-20">

        <h2 class="text-red-600 text-4xl">NUXT.JS PROJECT</h2>

        <p class="text-black-100 text-xl">For your information, working on one or two of your stats for a week gives you one point to the dashboard</p>

        <div class="bg-black border border-yellow-800 p-4 w-64 rounded-xl">
        
        <h2 class="text-yellow-600 text-lg font-semibold border-b border-yellow-800 pb-2 mb-3">
        Attributes
        </h2>
        <div class="flex flex-col gap-1">
        <div v-for="stat in stats" :key="stat.name" class="flex items-center justify-between px-3 py-3 hover:bg-yellow-900/20">
            <div class="flex items-center gap-2">
            <img :src="stat.icon" class="w-5 h-5" />
            <span class="text-yellow-200 text-sm">{{ stat.name }}</span>
            </div>
            <div class="flex items-center gap-2">
                <button @click="stat.value--" class="w-6 h-6 bg-yellow-900 text-yellow-200">
                    -
                </button>
                <span class="text-yellow-200 text-sm">{{ stat.value }}</span>
                <button @click="stat.value++" class="w-6 h-6 bg-yellow-900 text-yellow-200">
                    +
                </button>
            </div>
        </div>
        </div>
    </div>

    </div>

</template>
<script setup>


const stats = ref([
  { name: 'Attunement',   value: 1, icon: '/public/images/attunement_icon.jpg' },
  { name: 'Dexterity',    value: 1, icon: '/public/images/dexterity_icon.jpg' },
  { name: 'Endurance',    value: 1, icon: '/public/images/endurance_icon.jpg' },
  { name: 'Faith',        value: 1, icon: '/public/images/faith_icon.jpg' },
  { name: 'Intelligence', value: 1, icon: '/public/images/intelligence.jpg' },
  { name: 'Resistance',   value: 1, icon: '/public/images/resistance_icon.jpg' },
])

// function increment(stat){
//     stat.value++
// }

// function decrement(stat){
//     stat.value--
// }

</script>