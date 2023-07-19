<template>
  <kuba>
    <div
      class="w-full mt-[100px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4"
    >
      <div class="pb-[30px]">
        <div class="text-[32px] my-4 font-semibold text-center mb-5">
          Jakub Rzepka
        </div>
        <div
          class="text-black mt-1 text-center flex flex-col items-center mb-5"
        >
          <p class="font-semibold">
            Student 3 roku <span class="text-[#ff7f50]">Informatyki.</span>
            <br />
            Frontend <span class="text-[#ff7f50]">Developer.</span><br />
            Zajmuje się głównie technologiami Vue oraz
            <span class="text-[#ff7f50]">Nuxt.</span> <br />
            Zajął się również stworzeniem części
            <span class="text-[#ff7f50]">Frontend'ową.</span>
          </p>
          <span class="font-bold mb-5"></span>
          <a href="mailto:w64191@student.wsiz.edu.pl"
            >w64191@student.wsiz.edu.pl</a
          >
          <a href="https://github.com/Jqoobo">
            <Icon name="grommet-icons:github" size="50" class="mt-3" />
          </a>
        </div>
      </div>
    </div>
  </kuba>
</template>

<script setup>
import kuba from "@/layouts/kuba.vue";
</script>
