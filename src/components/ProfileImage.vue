<template>
 <section>
    <img :src="image" alt="profile" />
 </section>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
 user: {
    type: Object,
    required: true
 }
});
</script>
