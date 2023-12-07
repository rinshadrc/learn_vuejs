<template>
  <div>
    <h3>Goal manager</h3>
    <div>
      <label for="goal"></label>
      <input
        type="text"
        id="goal"
        v-model="enteredvalue"
        placeholder="Enter your Goal"
      />
      <button v-on:click="addgoal">Add goal</button>
    </div>
    <ul>
      <li>
        <h1 v-for="goal in goals" :key="goal">{{ goal }}</h1>
      </li>
    </ul>
  </div>

  <div class="main">
    <h1>Main component</h1>

    <div class="content">
      <User />
      <ProductList />
    </div>
  </div>
</template>


<script>

import User from "./User.vue";
import ProductList from "./Products.vue";

export default {
  name: "MainPage",
  components: {
    User,
    ProductList,
  },

  data() {
    return {
      goals: [],
      enteredvalue: "",
    };
  },

  methods: {
    addgoal() {
      this.goals.push(this.enteredvalue);
      this.enteredvalue = "";
    },
  }
};
</script>
<style>
.main {
  background: rgb(90, 90, 226);
  height: 300px;
  color: aliceblue;
}

.content {
  display: flex;

  flex-direction: column;
  margin: 10px;
}
</style>