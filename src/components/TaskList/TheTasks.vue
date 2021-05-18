<template>
  <base-card>
    <base-button
      @click="setSelectedTab('task-list')"
      :mode="storedResButtonMode"
    >
      Stored Resources
    </base-button>
    <base-button @click="setSelectedTab('add-task-item')" :mode="addResButtonMode">
      Add Resource
    </base-button>
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import TaskList from "./TaskList.vue";
import AddTaskItem from "./AddTaskItem";
export default {
  components: {
    TaskList,
    AddTaskItem,
  },
  data() {
    return {
      selectedTab: "task-list",
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
  provide() {
    return {
      tasks: this.tasks,
    };
  },
  computed: {
    storedResButtonMode() {
      return this.selectedTab === "task-list" ? null : "flat";
    },
    addResButtonMode() {
      return this.selectedTab === "add-task-item" ? null : "flat";
    },
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>

<style></style>
