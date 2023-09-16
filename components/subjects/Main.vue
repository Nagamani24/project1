
<template>
    <NuxtLink to="/subject/name">
        <button class="bg-blue-400 w-full py-2 m-3 ml-0 rounded-xl text-white text-md" >
            {{ props.subject }}
        </button>
    </NuxtLink>
</template>

<script lang="ts" setup>
const props=defineProps(['subject'])
</script>