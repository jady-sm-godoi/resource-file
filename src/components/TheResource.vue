<template>
  <content-display
    v-for="resource in resourcesFiles"
    :key="resource"
    :resource="resource"
  ></content-display>
</template>

<script>
import ContentDisplay from "./ContentDisplay/ContentDisplay.vue";

export default {
  //onde tudo se encontra!
  components: { ContentDisplay },
  data() {
    return {
      resourcesFiles: [
        {
          title: "Um breve exemplo de título",
          text:
            "    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          source: "https://loremipsum.io/",
        },
        {
          title: "Outro não tão breve exemplo de título",
          text:
            "    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          source: "https://loremipsum.io/",
        },
      ],
    };
  },
};
</script>
