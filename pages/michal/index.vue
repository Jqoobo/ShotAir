<template>
  <michal>
    <div
      class="w-full mt-[100px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4"
    >
      <div class="pb-[30px]">
        <div class="text-[32px] my-4 font-semibold text-center mb-5">
          Michał Lustyk
        </div>
        <div
          class="text-black mt-1 text-center flex flex-col items-center mb-5"
        >
          <p class="font-semibold">
            Student 3 roku <span class="text-[#ff7f50]">Informatyki.</span>
            <br />
            Blockchain <span class="text-[#ff7f50]">Developer.</span><br />
            Zajmuje się głównie technologiami
            <span class="text-[#ff7f50]">Blockchain.</span> <br />
            Zajął się również stworzeniem części
            <span class="text-[#ff7f50]">Backend'owej.</span>
          </p>
          <span class="font-bold mb-5"></span>
          <a href="mailto:w64885@student.wsiz.edu.pl"
            >w64885@student.wsiz.edu.pl</a
          >
          <a href="https://github.com/kacpulol">
            <Icon name="grommet-icons:github" size="50" class="mt-3" />
          </a>
        </div>
      </div>
    </div>
  </michal>
</template>

<script setup>
import michal from "@/layouts/michal.vue";
</script>
