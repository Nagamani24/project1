<template>
<div class="h-screen w-full p-8 bg-slate-100">
<div class="flex flex-col justify-start">
    <div class="font-roboto">
        <h1 class="text-lg text-slate-800">See the list of subjects available</h1>
        <p class="text-sm text-slate-400">Click on the subject you want to learn</p>
    </div>
</div>
<div  class="grid grid-cols-3 gap-3">
    <div v-for="(item,index) in subjects" :key="index">
        <SubjectsMain :subject="item"/>
    </div>
</div>
</div>

    
</template>
<script lang="ts" setup>
const subjects=['Physics','Chemistry','BEE','English']
</script>