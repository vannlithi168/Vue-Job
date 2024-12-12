<script>
export default {
  data() {
    return {
      name: "testing",
      status: "inactive",
      items: [
        { id: 1, name: "active", age: 12 },
        { id: 2, name: "pending", age: 17 },
        { id: 3, name: "inactive", age: 22 },
      ],
      link: "https://google.com",
    };
  },

  methods: {
    toggleStatus() {
      if (this.status === "active") {
        this.status = "inactive";
      } else if (this.status === "pending") {
        this.status = "active";
      } else {
        this.status = "pending";
      }
    },
  },
};
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>
  <!-- <h1 v-for="item in items" :key="item">
    {{ items }}
  </h1> -->

  <!-- <h3 v-if="items.length > 0">
    {{ items[0].id }}.{{ items[0].name }},{{ items[0].age }}
  </h3> -->

  <h4 v-for="(item, index) in items" :key="index">
    {{ index + 1 }}.{{ item.name }},{{ item.age }}
  </h4>

  <a v-bind:href="link">Redirect to Google || </a>
  <a :href="link" :style="'background-color: red; padding: 10px;'">Google</a>

  <button @click="toggleStatus">Change Status</button>
</template>

<style scoped></style>
