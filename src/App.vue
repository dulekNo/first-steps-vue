<template>
  <div>
    <h1>Llama project!</h1>
    <MyHeader />
    <ul>
      <li v-for="x in comments" v-bind:key="x.id" class="comment">
        <p>{{ x.name }}</p>
        <p>{{ x.content }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue";

export default {
  name: "App",
  components: {
    MyHeader
  },
  data() {
    return {
      comments: [
        {
          id: "0",
          name: "You",
          content: "yes"
        },
        {
          id: "1",
          name: "You 2",
          content: "something is no yes"
        },
        {
          id: "2",
          name: "You 3",
          content: "Thank you from mountain"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
h1 {
  color: #ffaabb;
}
.comment {
  background: #eee;
  list-style: none;
  padding: 5px;
  margin: 10px;

  p:first-child {
    font-weight: bold;
  }

  p:last-child {
    font-size: 20px;
  }
}
</style>
