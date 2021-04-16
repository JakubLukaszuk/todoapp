<template>
    <header>
        <h1>{{ title }}</h1>
    </header>
</template>

<script>
export default {
    props:{
        title:{
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>
header {
  width: 100%;
  height: 4.5rem;
  background-color: #29282e;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  display: flex;
  justify-content: center;
  align-items: center;
}

header h1 {
  color: white;
  margin: 0;
}
</style>