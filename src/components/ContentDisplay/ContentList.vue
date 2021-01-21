<template>
  <content-display
    v-for="res in resources"
    :key="res.id"
    :resource="res"
  ></content-display>
</template>

<script>
import ContentDisplay from "./ContentDisplay.vue";

export default {
  components: { ContentDisplay },
  inject: ["resources"],
};
</script>
