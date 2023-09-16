<template>
     <div class="flex flex-col mb-2 p-4">
                <div v-if="!open" class="flex items-center">
                    <i class="fab fa-font-awesome"></i>
                    <img src="https://play-lh.googleusercontent.com/y2Od7hvKRSTHUt4U-hTOFSp6clrrNK7JXGxjYur6ffCOypJpEcRX2HSRIgbuwjWPv54" class="h-8 w-8 m-3" />
                    <p  @click="open=!open">https://youtu.be/JieVY0q1Ypg</p>
                </div>

                    <div v-if="open" class="flex flex-col">
                    <iframe width="420" height="315"
                        src="https://www.youtube.com/embed/JieVY0q1Ypg?autoplay=1&mute=1">
                    </iframe>
                    <button class="bg-blue-400 py-2 m-3 rounded-xl text-white text-md justify-end" @click="open=false">Back</button>
                
                </div>
    </div>
</template>
<script lang="ts" setup>
const open = ref(false)
</script>