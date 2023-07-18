<template>
  <div class="flex border-b py-6">
    <div class="cursor-pointer"></div>
    <div class="pl-3 w-full px-4">
      <div class="flex flex-row items-center justify-between pb-2">
        <div class="flex flex-row">
          <img
            class="rounded-full max-h-[60px] mb-2 ml-1"
            width="60"
            src="assets\images\c635b669d116b4da3e9fa3f29517d41d.jpg"
          />
          <button class="mb-2 ml-2.5">
            <span class="font-bold hover:underline cursor-pointer">
              {{ item.user.name }}
            </span>
            <span
              class="text-[13px] text-light text-gray-500 pl-1 cursor-pointer"
            >
              @{{ item.user.username }}
            </span>
          </button>
        </div>
      </div>
      <div
        class="text-[17px] pb-1 pl-1 break-words md:max-w-[400px] max-w-[300px]"
      >
        {{ item.description }}
      </div>
      <div class="text-[12px] text-gray-500 pb-3 pl-1">
        {{ item.hashtags }}
      </div>
      <div class="mt-2.5 flex flex-col">
        <div
          class="relative min-h-[480px] max-h-[580px] w-full flex items-center cursor-pointer"
        >
          <iframe
            v-bind:src="item.url"
            frameborder="0"
            allowfullscreen="true"
            scrolling="no"
            height="600px"
            width="100%"
          ></iframe>
          <img
            class="absolute top-2 right-5"
            width="90"
            src="assets\images\shotAirLogo.svg"
          />
        </div>
        <div class="flex flex-row items-center">
          <div class="pt-6 pl-1 text-center flex flex-col">
            <button
              class="rounded-full bg-gray-200 p-2 cursor-pointer"
              @click="toggleLike(item.id, index)"
            >
              <Icon
                name="mdi:heart"
                size="25"
                :color="isLiked ? '#ff7f50' : ''"
                @click="question"
              />
            </button>
            <span class="text-xs text-gray-800 font-semibold pt-2">{{
              isLiked ? item.likeCounter + 1 : item.likeCounter
            }}</span>
          </div>
          <div
            class="bg-orange-100 border-l-4 border-orange-500 text-black p-4 mt-4 mb-4 mx-4 font-semibold"
            v-if="questionVisible"
          >
            <a class="text-[#ff7f50] hover:text-orange-600" href="/logowanie"
              >Zaloguj się</a
            >, aby móc polubić shota!
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      data: [],
      isLiked: false,
      questionVisible: false,
    };
  },

  props: {
    item: {
      type: Object,
      required: true,
    },
    index: {
      type: Number,
      required: true,
    },
  },

  methods: {
    async addLike(id, index) {
      const response = await axios.post(
        "http://localhost:8080/posts/like/" + id,
        {
          id: id,
        },
        {
          headers: {
            Authorization:
              "Bearer" + " " + localStorage.getItem("access_token"),
          },
        }
      );
      this.isLiked = true;
      console.log(this.item);
      console.log(response);
    },

    async removeLike(id, index) {
      const response = await axios.post(
        "http://localhost:8080/posts/unlike/" + id,
        {
          id: id,
        },
        {
          headers: {
            Authorization:
              "Bearer" + " " + localStorage.getItem("access_token"),
          },
        }
      );
      this.isLiked = false;
      console.log(this.item);
      console.log(response);
    },
    async toggleLike(id, index) {
      if (this.isLiked == false) {
        this.addLike(id, index);
      } else {
        this.removeLike(id, index);
      }
    },
    async question() {
      const jwt_token = localStorage.getItem("access_token");
      console.log(jwt_token);
      if (jwt_token == null) {
        this.questionVisible = true;
      }
    },
  },
};
</script>
