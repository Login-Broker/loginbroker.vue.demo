<template>
  <div class="App">
    <SessionButton platform="google"    @onSessionReceived="handleSessionReceived" @onErrorReceived="handleErrorReceived" />
    <SessionButton platform="github" @onSessionReceived="handleSessionReceived" @onErrorReceived="handleErrorReceived" />
  </div>
</template>
<script lang="ts">
import { SessionButton } from 'vue-login-broker-library';
import 'vue-login-broker-library/dist/style.css';

export default {
  components: {
    SessionButton,
  },
  methods: {
    handleSessionReceived(sessionId: any) {
      debugger
      console.log('Received sessionId', sessionId);
      // Perform further action
      // window.location.href = "https://login.broker/";
    },
    handleErrorReceived(error: any) {
      debugger
      console.log('Error happened', error);
    },
  },
};
</script>

<style scoped>
/* Your styles from 'App.css' can be added here */
</style>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
