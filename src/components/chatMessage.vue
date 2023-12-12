<script setup>
import { ref } from 'vue'

const chat_text = ref('')
</script>

<template>
    <div class="fixed-input-container">
      <q-input filled v-model="chat_text" label="Message to PlantScience.ai">
        <template v-slot:prepend>
          <q-icon name="smart_toy" />
        </template>
        <template v-slot:append>
          <q-icon name="send" color="teal" />
        </template>
      </q-input>
    </div>
</template>