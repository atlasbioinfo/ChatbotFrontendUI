<script setup>
import { ref } from 'vue'
import conversationSideBar from '@/components/conversationSideBar.vue';
import chatMessage from '@/components/chatMessage.vue';

const chat_text = ref('')
const conversationList_names = ref([
  'FLC functions',
  'Plant growth'
])
const chat_mode = ref(false)

</script>

<template>
  <q-drawer v-model="leftDrawerOpen" show-if-above bordered class="bg-grey-2" :width="240">
    <conversationSideBar :conversationListNames="conversationList_names" />
  </q-drawer>
  <q-page class="flex flex-center">

    <chatMessage />
  
  </q-page>
</template>

<style scoped>
.fixed-input-container {
  position: absolute;
  /* Position your input container absolutely */
  bottom: 20px;
  padding: 10px;
  width: 61.8%
}

.page-container {
  max-width: 600px;
}
</style>