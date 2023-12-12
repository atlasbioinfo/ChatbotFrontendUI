<script setup>
import { ref, defineProps } from 'vue'
const props = defineProps({
  conversationListNames: {
    type: Array,
    default: () => ['FLC functions', 'Flowering time', 'Plant growth']
  }
})

</script>

<template>
  <q-layout view="hHh lpR fFf">

    <q-header class="bg-grey-2 text-black q-mt-md">
      <q-list>
        <q-item v-ripple clickable>
          <q-item-section avatar>
            <q-icon name="add" />
          </q-item-section>
          <q-item-section>New Chat</q-item-section>
        </q-item>
        <q-separator class="q-my-md" />
      </q-list>
    </q-header>

    <q-page-container>
      <q-list>
        <q-item-label header class="text-weight-bold text-uppercase">
          Conversations
        </q-item-label>


        <q-item v-ripple clickable v-for="name in props.conversationListNames">

          <q-item-section>{{ name }}</q-item-section>
          <q-item-section avatar>
            <q-btn class="gt-xs" size="10px" flat dense round icon="more_horiz" />
          </q-item-section>
        </q-item>

      </q-list>
    </q-page-container>

    <q-footer class="bg-grey-2 text-black">
      <q-list>
        <q-separator class="q-my-md" />
        <q-item v-ripple clickable class="q-my-md">
          <q-item-section avatar>
            <q-btn class="gt-xs" size="10px" flat dense round icon="settings" />
          </q-item-section>
          <q-item-section>
            Settings
          </q-item-section>
        </q-item>
      </q-list>
    </q-footer>

  </q-layout>
</template>