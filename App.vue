<template>
  <div>
    <h2>Sign Up</h2>
    Email: {{ email }} / Password: {{ password }}
    <p><input type=" text" placeholder="Email" v-modul="email" /></p>
    <p><input type="password" placeholder="Password" v-modul="password" /></p>
    <p class="error-message" v-if="password.length < 6 >" >Your password must a last 6 character</p>
  </div>
</template>
<script>
export default {
  datd() {
    return {
      email: "",
      password: "",
    };
  },
};
</script>
<style ></style>




