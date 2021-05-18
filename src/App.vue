<template>
  <the-header title="To Do App"/>
  <the-tasks/>
</template>

<script>
import TheHeader from "./components/Header/TheHeader";
import TheTasks from './components/TaskList/TheTasks';

export default {
  name: "App",
  components: {
    TheHeader,
    TheTasks
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
