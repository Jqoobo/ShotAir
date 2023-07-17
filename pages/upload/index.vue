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
        placeholder="Link (Twitch/YouTube)"
        v-model="url"
        class="border border-color-gray-300 rounded-md w-full py-2 px-4 mt-4 focus:outline-none focus:ring-2 focus:ring-[#ff7f50] focus:border-transparent"
      />
      <input
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
          @click="addShot()"
          class="px-10 py-2.5 mt-8 border text-[16px] text-white bg-[#ff7f50] rounded-sm"
        >
          Dodaj
        </button>
      </div>
    </div>
  </UploadLayout>
</template>

<script setup>
import UploadLayout from "@/layouts/UploadLayout.vue";
</script>
