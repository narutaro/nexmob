<template>
  <v-ons-page>
    <div class="login-form">
      <p><v-ons-input v-model="form.name" id="username" modifier="underbar" placeholder="Username" float></v-ons-input></p>
      <p><v-ons-input v-model="form.password" id="password" modifier="underbar" type="password" placeholder="Password" float></v-ons-input></p>
      <v-ons-button @click="login">login</v-ons-button>
    </div>
  </v-ons-page>
</template>

<script>
export default {
  methods: {
    login() {
      console.log("login clicked");
      //pageStack.push(P1);
    }
  },
  data() {
    return {
      form: {
        name: '',
        password: ''
      }
    }
  }
}
</script>

<style scoped>
.login-form {
  text-align: center;
  margin-top: 200px;
}
</style>