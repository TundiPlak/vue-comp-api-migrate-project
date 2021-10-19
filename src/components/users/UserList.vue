<template>
  <base-container>
    <h2>Active Users</h2>
    <base-search @search="updateSearch" :search-term="enteredSearchTerm" />
    <div>
      <button>Sort Ascending</button>
      <button>Sort Descending</button>
    </div>
    <ul>
      <user-item
        v-for="user in users"
        :key="user.id"
        :user-name="user.fullName"
        :id="user.id"
      />
    </ul>
  </base-container>
</template>

<script>
import UserItem from "./UserItem.vue";
export default {
  name: "UserList",
  component: {
    UserItem,
  },
  props: ["users"],
  data() {
    return {
      enteredSearchTerm: "",
      activeSearchTerm: "",
      sorting: null,
      loading: false,
    };
  },
  computed: {
    availableUsers() {
      let users = [];
      if (this.activeSearchTerm) {
        users = this.users.filter((usr) => {
          usr.fullName.includes(this.activeSearchTerm);
        });
      } else if (this.users) {
        users = this.users;
      }
      return users;
    },
  },
  methods: {},
};
</script>
