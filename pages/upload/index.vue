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
      <div
        class="bg-orange-100 border-l-4 border-orange-500 text-orange-700 p-4 my-2"
        v-if="error"
      >
        <p class="font-semibold">{{ error }}</p>
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
      <input
        v-model="hashtags"
        placeholder="Hashtagi"
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
      hashtags: "",
      error: "",
    };
  },
  methods: {
    async addShot() {
      try {
        if (this.url.includes("twitch.tv")) {
          console.log(this.url);
          const url = this.url;
          const t = new URL(url);
          const saplitedPathname = t.pathname.split("/");
          const clipID = t.pathname.split("/")[saplitedPathname.length - 1];
          const twitchURL = `https://clips.twitch.tv/embed?clip=${clipID}&parent=localhost`;

          const response = await axios.post(
            "http://localhost:8080/posts",
            {
              url: twitchURL,
              description: this.description,
              hashtags: this.hashtags,
            },
            {
              headers: {
                Authorization:
                  "Bearer" + " " + localStorage.getItem("access_token"),
              },
            }
          );
          console.log(response);
          this.$router.push("/");
        } else if (this.url.includes("youtu.be")) {
          const url = "https://youtu.be/vEO45dRkGwk";
          const y = new URL(url);
          const saplitedPathname = y.pathname.split("/");
          const clipID = y.pathname.split("/")[saplitedPathname.length - 1];
          const ytURL = `https://www.youtube.com/embed/${clipID}`;

          const response = await axios.post(
            "http://localhost:8080/posts",
            {
              url: ytURL,
              description: this.description,
              hashtags: this.hashtags,
            },
            {
              headers: {
                Authorization:
                  "Bearer" + " " + localStorage.getItem("access_token"),
              },
            }
          );
          console.log(response);
          this.$router.push("/");
        } else {
          this.error = "Błędne dane lub nie wprowadzono wszystkich danych";
        }
      } catch (e) {
        this.error = "Błędne dane lub nie wprowadzono wszystkich danych";
      }
    },
  },
};
</script>
