<template>
  <li>
    <base-card>
      <div>
        <header>
          <h3>{{ title }}</h3>
          <button>Delete</button>
        </header>
      </div>
      <p>{{ description }}</p>
      <nav v-if="link">
        <a :href="link">link</a>
      </nav>
    </base-card>
  </li>
</template>

<script>
import BaseCard from "../UI/BaseCard.vue";
export default {
  components: { BaseCard },
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      required: false,
    },
  },
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
  color: #d36912;
}

a:hover,
a:active {
  color: #d6ab1c;
}
</style>