<template>
  <Register-layout>
    <div
      class="w-full mt-[100px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4"
    >
      <div>
        <div class="text-[23px] font-semibold text-center">Rejestracja</div>
        <div class="text-gray-400 mt-1 text-center">
          Zarejestruj się, aby móc dodawać shota
        </div>
      </div>
      <div
        class="bg-orange-100 border-l-4 border-orange-500 text-orange-700 p-4 my-2"
        v-if="error"
      >
        <p class="font-bold">{{ error }}</p>
      </div>
      <input
        v-model="name"
        placeholder="Nazwa"
        class="border border-color-gray-300 rounded-md w-full py-2 px-4 mt-4 focus:outline-none focus:ring-2 focus:ring-[#ff7f50] focus:border-transparent"
      />
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
      <div class="mx-1 my-2 text-center">
        <a class="text-gray-500 mt-1"
          >Hasło musi zawierać
          <span class="text-[#ff7f50]">literę (np.a)</span>,
          <span class="text-[#ff7f50]">znak specjalny (np.$)</span> oraz
          <span class="text-[#ff7f50]">liczbę(np.1)</span>!</a
        >
      </div>
      <div class="flex gap-3 justify-center">
        <button
          @click="register"
          class="px-10 py-2.5 mt-8 border text-[16px] text-white bg-[#ff7f50] rounded-sm"
        >
          Zarejestruj
        </button>
      </div>
    </div>
  </Register-layout>
</template>

<script>
import RegisterLayout from "@/layouts/RegisterLayout.vue";
import axios from "axios";

export default {
  components: {
    RegisterLayout,
  },
  data() {
    return {
      name: "",
      username: "",
      password: "",
      error: "",
    };
  },
  methods: {
    async register() {
      try {
        const response = await axios.post("http://localhost:8080/auth/signin", {
          name: this.name,
          username: this.username,
          password: this.password,
        });
        console.log(response);
        this.$router.push("/");
      } catch (e) {
        this.error = "Użytkownik o takim nicku już istnieje";
      }
    },
  },
};
</script>
