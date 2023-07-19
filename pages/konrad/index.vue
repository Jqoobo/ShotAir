<template>
  <konrad>
    <div
      class="w-full mt-[100px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4"
    >
      <div class="pb-[30px]">
        <div class="text-[32px] my-4 font-semibold text-center mb-5">
          Konrad Rzepka
        </div>
        <div
          class="text-black mt-1 text-center flex flex-col items-center mb-5"
        >
          <p class="font-semibold">
            Student 3 roku <span class="text-[#ff7f50]">Informatyki.</span>
            <br />
            Zajął się stworzeniem części
            <span class="text-[#ff7f50]">dokumentacji.</span>
          </p>
          <span class="font-bold mb-5"></span>
          <a href="mailto:w64885@student.wsiz.edu.pl"
            >w64885@student.wsiz.edu.pl</a
          >
          <a href="https://github.com/">
            <Icon name="grommet-icons:github" size="50" class="mt-3" />
          </a>
        </div>
      </div>
    </div>
  </konrad>
</template>

<script setup>
import konrad from "@/layouts/konrad.vue";
</script>
