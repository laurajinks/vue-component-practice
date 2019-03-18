<template>
  <div class="col-xs-12 col-sm-6">
    <ul class="list-group" v-for="server in servers" :key="server.id">
      <ListItem :server="server"/>
    </ul>
  </div>
</template>

<script>
import ListItem from "./ListItem";

export default {
  name: "ServerStatus",
  components: {
    ListItem
  },
  data: function() {
    return {
      servers: [
        { id: 1, status: "Normal" },
        { id: 2, status: "Critical" },
        { id: 3, status: "Unknown" },
        { id: 4, status: "Normal" }
      ]
    };
  }
};
</script>