
<template>
    <div class="flex w-full h-screen mt-5">
   <div class="w-[30%] flex flex-col  border border-2 p-3">
    <div v-for="(item,index) in props.subjects" :key="index">

    <button class="bg-blue-400 w-full py-2 m-3 ml-0 rounded-xl text-white text-md" @click="select(item)">
            {{ item }}
        </button>
   </div>
</div>
      <div class="border border-2 w-[70%] ml-5">
   <SubjectsTopics v-show="onclick" :selectedSubject="selectedSubject"/>

      </div> 
</div>
</template>

<script lang="ts" setup>
const props=defineProps(['subjects'])
const onclick=ref(false)
const selectedSubject=ref('')

const select = (sub:string)=>{
    onclick.value=true
selectedSubject.value=sub

}
</script>