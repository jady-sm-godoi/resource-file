<template>
  <div>
    <base-card>
      <template #default>
        <header>
          <h3>{{ resource.title }}</h3>
          <base-button>Delete</base-button>
        </header>
        <p>{{ resource.text }}</p>
        <a>{{ resource.source }}</a>
      </template>
    </base-card>
  </div>
</template>

<script>
export default {
  props: { resource: Object },
  //conteúdo
};
</script>

<style scoped>
li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}
</style>
