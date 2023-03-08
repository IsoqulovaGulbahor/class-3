<template>
  <div id="list-demo">
    <button class="first-button" @click="add">Add</button>
    <div class="img"></div>
    <button class="second-button" @click="remove">Remove</button>
    <transition-group name="list" teg="ul">
      <li v-for="item in items" :key="item.id" class="list-item">
        Item: {{ item - 1 }} - {{ item }} =
      </li>
    </transition-group>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [1, 2, 3],
      nextNum: 10,
    };
  },
  methods: {
    randomItem() {
      return Math.floor(Math.random() * this.items.length);
    },
    add() {
      this.items.splice(this.randomItem(), 0, this.nextNum++);
    },
    remove() {
      this.items.splice(this.randomItem(), 1);
    },
  },
};
</script>
<style>
* {
  padding: 0;
  margin: 0;
}
body {
  margin: 50px;
}
.list-item {
  display: inline-block;
  display: block;
  width: 30%;
  background-color: rgb(252, 173, 147);
}
.img {
  width: 200px;
  height: 300px;
  background-image: url(Childern.jpg);
  border-radius: 10px;
}
button {
  padding: 15px 10px;
  transition: all;
}
.first-button {
  border: 1px solid red;
  border-radius: 50%;
}
.second-button {
  border: 1px solid green;
  border-radius: 50%;
}
</style>
