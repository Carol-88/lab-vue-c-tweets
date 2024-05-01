<template>
 <section>
    <img :src="image" class="profile" alt="profile" />
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
