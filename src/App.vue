<template>
  <main>
    <img alt="Vue logo" src="./assets/logo.png" />
    <user-list :users="activeUsers" />

    <project-list></project-list>
  </main>
</template>

<script>
import USER_DATA from "./dummy-data.js";
import UserList from "./components/users/UserList.vue";
import ProjectList from "./components/projects/ProjectList.vue";

export default {
  name: "App",
  components: {
    UserList,
    ProjectList,
  },
  data() {
    return {
      activeUsers: USER_DATA,
      selectedUser: null,
      /*users: [
        {
          id: "max",
          fullName: "Max Schwarz",
          projects: [
            { id: "max_p1", title: "Project1" },
            { id: "max_p2", title: "Project2" },
            { id: "max_p3", title: "Project3" },
          ],
        },
        {
          id: "sohie",
          fullName: "Sophie Brown",
          projects: [
            { id: "sophie_p1", title: "Thesis1" },
            { id: "sophie_p2", title: "Thesis2" },
            { id: "sophie_p3", title: "Thesis3" },
          ],
        },
        {
          id: "dan",
          fullName: "Dan Lorenta",
          projects: [
            { id: "dan_p1", title: "Book1" },
            { id: "dan_p2", title: "Book2" },
          ],
        },
        {
          id: "cody",
          fullName: "Cody Plant",
          projects: [],
        },
      ], */
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
