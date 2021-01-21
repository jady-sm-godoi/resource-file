<template>
  <base-card>
    <base-button @click="changeComponent('content-list')"
      >Resources</base-button
    >
    <base-button @click="changeComponent('content-form')"
      >New Resource</base-button
    >
  </base-card>
  <component :is="whatComponent"> </component>
</template>

<script>
import ContentList from "./ContentDisplay/ContentList.vue";
import ContentForm from "./ContentDisplay/ContentForm.vue";

export default {
  //onde tudo se encontra!
  components: { ContentList, ContentForm },
  data() {
    return {
      whatComponent: "content-list",
      resourcesFiles: [
        {
          id: 1,
          title: "Um breve exemplo de título",
          text:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          source: "https://loremipsum.io/",
        },
        {
          id: 2,
          title: "Outro não tão breve exemplo de título",
          text:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          source: "https://loremipsum.io/",
        },
      ],
    };
  },
  provide() {
    return { resources: this.resourcesFiles };
  },
  methods: {
    changeComponent(comp) {
      this.whatComponent = comp;
    },
  },
};
</script>
