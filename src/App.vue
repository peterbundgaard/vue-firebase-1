<template>
  <v-app>
    <v-content>
      <v-layout align-center justify-center row fill-height v-if="routing">
        <v-progress-circular :size="70" :width="7" color="primary" indeterminate/>
      </v-layout>
      <snackbar/>
      <router-view v-show="!routing"/>
    </v-content>
  </v-app>
</template>

<script>
import { mapState } from 'vuex'
import Snackbar from '@/components/snackbar'

export default {
  name: 'app',
  computed: mapState(['routing']),
  components: {
    Snackbar
  }
}
</script>
