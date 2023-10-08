<template>
<div class="h-screen w-full p-8 bg-slate-100">
<div class="flex flex-col justify-start">
    <div class="font-roboto">
        <h1 class="text-lg text-slate-800">See the list of subjects & topics available</h1>
        <p class="text-sm text-slate-400">Click on the subject to see topics</p>
    </div>
</div>
        <SubjectsMain :subjects="subjects"/>
</div>

    
</template>
<script lang="ts" setup>
const subjects=['Physics','Chemistry','BEE','English']
</script>