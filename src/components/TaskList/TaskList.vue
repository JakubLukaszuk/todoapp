<template>
  <ul>
    <task-item
      v-for="task in tasks"
      :key="task.id"
      :title="task.title"
      :description="task.description"
      :link="task.link"
    ></task-item>
  </ul>
</template>

<script>
import TaskItem from "./TaskItem";

export default {
  props: {
    tasks:{
      type: Array,
      required: true
    }
  },
  components: {
    TaskItem,
  },
};
</script>

<style scoped>
ul {
  margin: auto;
  max-width: 40rem;
}
</style>