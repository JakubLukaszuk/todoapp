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
  name: "App",
  components: {
    TaskItem,
  },
  data() {
    return {
      tasks: [
        {
          id: "official-guide",
          title: "Official Guide",
          description: "The offcial Vue documentation",
          link: "https://vuejs.org/",
        },
        {
          id: "google",
          title: "Google",
          description: "search engine",
          link: "https://www.google.com/",
        },
      ],
    };
  },
};
</script>