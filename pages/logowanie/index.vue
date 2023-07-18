<template>
  <login-layout>
    <div
      class="w-full mt-[100px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4"
    >
      <div>
        <div class="text-[23px] font-semibold text-center">Logowanie</div>
        <div class="text-gray-400 mt-1 text-center">
          Zaloguj się, aby móc dodawać shota
        </div>
      </div>
      <div
        class="bg-orange-100 border-l-4 border-orange-500 text-orange-700 p-4 my-2"
        v-if="error"
      >
        <p class="font-bold">{{ error }}</p>
      </div>
      <input
        v-model="username"
        placeholder="Nickname"
        max-length="100"
        class="border border-color-gray-300 rounded-md w-full h-[60px] py-2 px-4 mt-4 focus:outline-none focus:ring-2 focus:ring-[#ff7f50] focus:border-transparent"
      />
      <input
        v-model="password"
        placeholder="Hasło"
        max-length="100"
        class="border border-color-gray-300 rounded-md w-full h-[60px] py-2 px-4 mt-4 focus:outline-none focus:ring-2 focus:ring-[#ff7f50] focus:border-transparent"
      />
      <div class="mx-1 text-center text-gray-500 mt-3">
        Nie masz konta?<a
          href="/rejestracja"
          class="text-[#ff7f50] hover:text-[#16dbff] transition-all"
        >
          Zarejestruj się!</a
        >
      </div>
      <div class="mx-1 my-2 text-center"></div>
      <div class="flex gap-3">
        <button
          @click="login"
          class="px-10 py-2.5 mt-8 border text-[16px] text-white bg-[#ff7f50] rounded-sm"
        >
          Zaloguj się
        </button>
      </div>
    </div>
  </login-layout>
</template>

<script>
import LoginLayout from "@/layouts/LoginLayout.vue";
import axios from "axios";

export default {
  components: {
    LoginLayout,
  },
  data() {
    return {
      username: "",
      password: "",
      error: "",
    };
  },
  methods: {
    async login() {
      try {
        const response = await axios.post("http://localhost:8080/auth/login", {
          username: this.username,
          password: this.password,
        });
        console.log(response);
        localStorage.setItem("access_token", response.data.access_token);
        this.$router.push("/");
      } catch (e) {
        this.error = "Użytkownik nie istnieje lub wprowadzono błędne dane!";
      }
    },
  },
};
</script>
