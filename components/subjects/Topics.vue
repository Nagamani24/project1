<template>
    <div v-for="(item,index) in list" :key="index" class="p-5">
        <div v-for="(unit,index) in item.subjectTopics" :key="index">
            <h1 class="font-semibold">Unit - {{ unit.unit }}</h1>
            <ul v-for="(topic,index) in unit.topics" :key="index">
                <NuxtLink :to="`/subject/${topic.name.toLowerCase().split(' ,/-')[0]}-${topic.id}`">
                <li class="list-disc ml-8">{{ topic.name }}</li>
                </NuxtLink>
            </ul>
        </div>
    </div>
</template>

<script setup lang="ts">
import {list} from '../../data/subjectTopics.json'
const props=defineProps(['selectedSubject'])
</script>