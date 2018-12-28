<template>
  <v-ons-navigator swipeable :page-stack="pageStack" @push-page="pageStack.push($event)">
  </v-ons-navigator>
</template>

<script>
  import login_page from './login.vue'
  export default {
    data() {
      return {
        pageStack: [login_page]
      }
    }
  }
</script>