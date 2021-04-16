<template>
  <li>
    <div>
      <header>
        <h3>{{title}}</h3>
        <button>Delete</button>
      </header>
    </div>
    <p>{{description}}</p>
    <nav v-if="link">
        <a :href="link">link</a>
    </nav>
  </li>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true
        },
        link: {
            type: String,
            required: false
        },
    }
}
</script>