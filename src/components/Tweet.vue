<script setup>
import { defineProps } from 'vue';
import ProfileImage from './ProfileImage.vue'
import TimeStamp from './TimeStamp.vue'
import Message from './Message.vue'
import User from './User.vue'

 const props = defineProps({
 tweet: {
    type: Object,
    required: true
 }
});

</script>

<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />
    

    <div class="body">
      <div class="top">
       <User :userData="tweet.user" />

       <TimeStamp :timestamp="tweet.timestamp" />
      </div>

      <Message :message="tweet.message" />

      <div class="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>




<style scoped>
a {
  color: #42b983;
}
</style>
