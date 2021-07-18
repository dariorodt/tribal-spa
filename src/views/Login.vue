<template>
  <div>
    <pre>{{ user }}</pre>
    <form @submit.prevent="login">
      <input v-model="form.email" type="email" placeholder="Email" /> <br />
      <input v-model="form.password" type="password" placeholder="Password" />
      <br />
      <button>Login</button>
    </form>
  </div>
</template>

<script>
export default {
  data: () => ({
    user: {},
    form: {
      email: "",
      password: "",
    },
  }),
  methods: {
    login() {
      console.log("Enviando el login", this.form);
    },
  },
};
</script>

<style lang="scss" scoped></style>
