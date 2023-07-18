<template>
  <Post
    v-for="(item, index) in data"
    :key="item.id"
    :item="item"
    :index="index"
  />
</template>

<script>
import axios from "axios";
import Post from "@/components/Post.vue";

export default {
  components: {
    Post,
  },
  data() {
    return {
      data: [],
    };
  },
  methods: {
    async getItem() {
      axios.get("http://localhost:8080/posts").then((response) => {
        this.data = response.data;
        console.log(response);
      });
    },
  },
  async mounted() {
    this.getItem();
  },
};
</script>
