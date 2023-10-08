<template>
   <SubjectsVideos :id="id"/>
</template>
<script setup lang="ts">
import {  useRoute } from 'vue-router'

const id=useRoute().params.id

</script>