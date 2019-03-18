<template>
  <li
    class="list-group-item"
    style="cursor: pointer"
    @click="serverSelected"
  >Server #{{ server.id }}</li>
</template>

<script>
import { serverBus } from "../main.js";
export default {
  name: "ListItem",
  props: ["server"],
  data: function() {
    return {};
  },
  methods: {
    serverSelected() {
      serverBus.$emit("serverSelected", this.server);
    }
  }
};
</script> 