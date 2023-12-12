<script setup>

import { useQuasar } from 'quasar'

const $q = useQuasar()
</script>

<template>

  <q-layout view="hHh lpR fFf" class="bg-grey-1">
    <q-header elevated class="bg-white text-grey-8 q-py-xs" height-hint="58">
      <q-toolbar>
        <q-btn flat no-caps no-wrap class="q-ml-xs" v-if="$q.screen.gt.xs">
          <img src="@/assets/img/logo_small.png" alt="Logo" style="width: 28px; height: 28px;">
          <q-toolbar-title shrink class="text-weight-bold">
            PlantScience.ai
          </q-toolbar-title>
        </q-btn>
        <q-space />
        <div class="q-gutter-sm row items-center no-wrap">
          
          <q-btn round dense flat color="grey-8" icon="cloud_upload" v-if="$q.screen.gt.sm">
            <q-tooltip>Upload knowledge</q-tooltip>
          </q-btn>
          <q-btn round dense flat color="grey-8" icon="message" v-if="$q.screen.gt.sm">
            <q-tooltip>Messages</q-tooltip>
          </q-btn>
          <q-btn round dense flat color="grey-8" icon="help">
            <q-tooltip>Help</q-tooltip>
          </q-btn>
          <q-btn round flat>
            <q-avatar size="26px">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
            </q-avatar>
            <q-tooltip>Account</q-tooltip>
          </q-btn>
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>

  <!-- <RouterView /> -->
</template>

<style scoped>
.fixed-input-container {
  position: absolute;
  /* Position your input container absolutely */
  bottom: 100px;
  padding: 10px;
  width: 100%;
}
</style>
