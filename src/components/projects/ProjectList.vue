<template>
  <base-container>
    <h2>Name: Projects</h2>
    <base-search></base-search>
    <ul>
      <project-item></project-item>
    </ul>
  </base-container>
</template>

<script>
import ProjectItem from "./ProjectItem.vue";
export default {
  name: "ProjectList",
  component: {
    ProjectItem,
  },
};
</script>
