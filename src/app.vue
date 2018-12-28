<template>
  <v-ons-navigator swipeable :page-stack="pageStack" @push-page="pageStack.push($event)">
  </v-ons-navigator>
</template>

<script>
  function createURLSearchParams(data) {
    const params = new URLSearchParams();
    Object.keys(data).forEach(key => params.append(key, data[key]));
    return params;
  }
</script>

<script>
import login from './login.vue'
export default {
  data() {
    return {
      pageStack: [login]
    }
  }
}
</script>