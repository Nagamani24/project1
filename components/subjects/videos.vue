<template>
    <div v-if="props.id" class="flex flex-col mb-2 p-4">
               <div v-if="!open" class="flex items-center">
                   <img src="https://play-lh.googleusercontent.com/y2Od7hvKRSTHUt4U-hTOFSp6clrrNK7JXGxjYur6ffCOypJpEcRX2HSRIgbuwjWPv54" class="h-8 w-8 m-3" />
                   <p  @click="open=!open" class="cursor-pointer">https://youtu.be/{{ props.id }}</p>
               </div>

                   <div v-if="open" class="flex flex-col">
                   <iframe width="420" height="315"
                       :src="`https://www.youtube.com/embed/${props.id}?autoplay=1&mute=1`">
                   </iframe>
                   <div class="flex justify-end">
                   <button class="bg-blue-400 py-2 mt-3 rounded-xl text-white text-md justify-end w-[25%] ml-auto" @click="open=false">Back</button>
                </div>
               
               </div>
   </div>
</template>
<script lang="ts" setup>
const open = ref(false)
const props=defineProps(['id'])
</script>