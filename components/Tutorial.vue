<!-- Please remove this file from your project -->
<template>
  <div>
    <div v-if="$auth.user">
      {{$auth.user.name}}
    </div>
    <a v-if="$auth.loggedIn" @click="$auth.logout()">Sign Off</a>
    <a v-else @click="$auth.loginWith('auth0')">Sign In</a>
  </div>
</template>

<script>
export default {
  name: "NuxtTutorial",
};
</script>
