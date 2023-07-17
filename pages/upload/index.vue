<template>
  <UploadLayout>
    <div
      class="w-full mt-[100px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4"
    >
      <div>
        <div class="text-[23px] font-semibold">Dodaj shota</div>
        <div class="text-gray-400 mt-1">
          Dodaj shota, które przypisze się do twojego konta
        </div>
      </div>
      <input
        v-model="url"
        placeholder="Link (Twitch/YouTube)"
        class="border border-color-gray-300 rounded-md w-full py-2 px-4 mt-4 focus:outline-none focus:ring-2 focus:ring-[#ff7f50] focus:border-transparent"
      />
      <input
        v-model="description"
        placeholder="Opis"
        max-length="100"
        class="border border-color-gray-300 rounded-md w-full h-[60px] py-2 px-4 mt-4 focus:outline-none focus:ring-2 focus:ring-[#ff7f50] focus:border-transparent"
      />
      <div class="flex gap-3">
        <a href="/">
          <button
            class="px-10 py-2.5 mt-8 border text-[16px] hover:bg-gray-100 rounded-sm"
          >
            Wróć na stronę główną
          </button>
        </a>
        <button
          @click="addShot"
          class="px-10 py-2.5 mt-8 border text-[16px] text-white bg-[#ff7f50] rounded-sm"
        >
          Dodaj
        </button>
      </div>
    </div>
  </UploadLayout>
</template>

<script>
import UploadLayout from "@/layouts/UploadLayout.vue";
import axios from "axios";

export default {
  components: {
    UploadLayout,
  },
  data() {
    return {
      url: "",
      description: "",
    };
  },
  methods: {
    async addShot() {
      const url = this.url;
      const u = new URL(url);
      const saplitedPathname = u.pathname.split("/");
      const clipID = u.pathname.split("/")[saplitedPathname.length - 1];
      const newUrl = `https://clips.twitch.tv/embed?clip=${clipID}&parent=localhost`;

      const response = await axios.post(
        "http://localhost:8080/posts",
        {
          url: newUrl,
          description: this.description,
        },
        {
          headers: {
            Authorization:
              "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InppbWExIiwidXNlcklkIjoiMzYxN2I4MzctOTJiNC00NDBjLTgwYWYtMjA2ZTZlZDYzMDRjIiwiaWF0IjoxNjg5NjMxNzgwLCJleHAiOjE2ODk2Mzc3ODB9.NDiVDTvwLNTIPKtJ7hYZfbW4ShdHRNOO85JUsLtaqx4",
          },
        }
      );
      console.log(response);
      this.$router.push("/");
    },
  },
};
</script>
