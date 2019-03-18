<template>
  <div class="col-xs-12 col-sm-6">
    <p v-if="!server">Please select a server</p>
    <p v-else>Server Status: {{ server.status }}</p>
    <hr>
    <button v-if="server && server.status !== 'Normal'" @click="resetStatus ">Change to Normal</button>
  </div>
</template>

<script>
import { serverBus } from "../main.js";
export default {
  name: "ServerDetails",
  created() {
    serverBus.$on("serverSelected", server => {
      this.server = server;
    });
  },
  data: function() {
    return {
      server: null
    };
  },
  methods: {
    resetStatus() {
      this.server.status = "Normal";
    }
  }
};
</script>