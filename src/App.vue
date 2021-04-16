<template>
  <the-header title="To Do App"/>
  <task-list :tasks="tasks"/>
</template>

<script>
import TaskList from "./components/TaskList/TaskList";
import TheHeader from "./components/Header/TheHeader";

export default {
  name: "App",
  components: {
    TaskList,
    TheHeader
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

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
  list-style: none;
  margin: 0;
  padding: 0;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>
