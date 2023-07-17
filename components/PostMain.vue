<template>
  <div id="PostMain" class="flex border-b py-6">
    <div class="cursor-pointer"></div>
    <div class="pl-3 w-full px-4">
      <div class="flex flex-row items-center justify-between pb-2">
        <div class="flex flex-row">
          <img
            class="rounded-full max-h-[60px] mb-2"
            width="60"
            src="assets\images\c635b669d116b4da3e9fa3f29517d41d.jpg"
          />
          <button class="mb-2 ml-2">
            <span class="font-bold hover:underline cursor-pointer"> Kuba </span>
            <span
              class="text-[13px] text-light text-gray-500 pl-1 cursor-pointer"
            >
              @kuba_rzz
            </span>
          </button>
        </div>
        <button
          class="border text-[15px] px-[21px] py-0.5 border-[#ff7f50] text-[#ff7f50] hover:bg-[#ffeef2] font-semibold rounded-md"
        >
          Obserwuj
        </button>
      </div>
      <div
        class="text-[17px] pb-0.5 break-words md:max-w-[400px] max-w-[300px]"
      >
        Widzowie oszukują
      </div>
      <div class="text-[12px] text-gray-500 pb-0.5">
        #Platynov #gtarp #twitch
      </div>
      <div class="mt-2.5 flex flex-col">
        <div
          class="relative min-h-[480px] max-h-[580px] w-full flex items-center cursor-pointer"
        >
          <iframe
            v-bind:src="Url"
            frameborder="0"
            allowfullscreen="true"
            scrolling="no"
            height="480"
            width="665"
          ></iframe>
          <img
            class="absolute right-5 top-5"
            width="90"
            src="assets\images\shotAirLogo.svg"
          />
        </div>
        <div class="flex flex-row">
          <div class="pt-4 pr-4 text-center flex flex-col">
            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
              <Icon
                name="mdi:heart"
                size="25"
                :color="isLiked ? '#F02C56' : ''"
              />
            </button>
            <span class="text-xs text-gray-800 font-semibold pt-2">43</span>
          </div>
          <div class="pt-4 pr-4 text-center flex flex-col">
            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
              <Icon
                name="ri:share-forward-fill"
                size="25"
                :color="isLiked ? '#F02C56' : ''"
              />
            </button>
            <span class="text-xs text-gray-800 font-semibold pt-2">43</span>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div id="PostMain" class="flex border-b py-6">
    <div class="cursor-pointer"></div>
    <div class="pl-3 w-full px-4">
      <div class="flex flex-row items-center justify-between pb-2">
        <div class="flex flex-row">
          <img
            class="rounded-full max-h-[60px] mb-2"
            width="60"
            src="assets\images\c635b669d116b4da3e9fa3f29517d41d.jpg"
          />
          <button class="mb-2 ml-2">
            <span class="font-bold hover:underline cursor-pointer">
              Kacper
            </span>
            <span
              class="text-[13px] text-light text-gray-500 pl-1 cursor-pointer"
            >
              @kacpulol
            </span>
          </button>
        </div>
        <button
          class="border text-[15px] px-[21px] py-0.5 border-[#ff7f50] text-[#ff7f50] hover:bg-[#ffeef2] font-semibold rounded-md"
        >
          Obserwuj
        </button>
      </div>
      <div
        class="text-[17px] pb-0.5 break-words md:max-w-[400px] max-w-[300px]"
      >
        Widzowie oszukują
      </div>
      <div class="text-[12px] text-gray-500 pb-0.5">
        #Platynov #gtarp #twitch
      </div>
      <div class="mt-2.5 flex flex-col">
        <div
          class="relative min-h-[480px] max-h-[580px] w-full flex items-center cursor-pointer"
        >
          <iframe
            v-bind:src="Url"
            frameborder="0"
            allowfullscreen="true"
            scrolling="no"
            height="480"
            width="665"
          ></iframe>
          <img
            class="absolute right-5 top-5"
            width="90"
            src="assets\images\shotAirLogo.svg"
          />
        </div>
        <div class="flex flex-row">
          <div class="pt-4 pr-4 text-center flex flex-col">
            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
              <Icon
                name="mdi:heart"
                size="25"
                :color="isLiked ? '#F02C56' : ''"
              />
            </button>
            <span class="text-xs text-gray-800 font-semibold pt-2">43</span>
          </div>
          <div class="pt-4 pr-4 text-center flex flex-col">
            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
              <Icon
                name="ri:share-forward-fill"
                size="25"
                :color="isLiked ? '#F02C56' : ''"
              />
            </button>
            <span class="text-xs text-gray-800 font-semibold pt-2">43</span>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div id="PostMain" class="flex border-b py-6">
    <div class="cursor-pointer"></div>
    <div class="pl-3 w-full px-4">
      <div class="flex flex-row items-center justify-between pb-2">
        <div class="flex flex-row">
          <img
            class="rounded-full max-h-[60px] mb-2"
            width="60"
            src="assets\images\c635b669d116b4da3e9fa3f29517d41d.jpg"
          />
          <button class="mb-2 ml-2">
            <span class="font-bold hover:underline cursor-pointer">
              Michał
            </span>
            <span
              class="text-[13px] text-light text-gray-500 pl-1 cursor-pointer"
            >
              @pu0258
            </span>
          </button>
        </div>
        <button
          class="border text-[15px] px-[21px] py-0.5 border-[#ff7f50] text-[#ff7f50] hover:bg-[#ffeef2] font-semibold rounded-md"
        >
          Obserwuj
        </button>
      </div>
      <div
        class="text-[17px] pb-0.5 break-words md:max-w-[400px] max-w-[300px]"
      >
        Widzowie oszukują
      </div>
      <div class="text-[12px] text-gray-500 pb-0.5">
        #Platynov #gtarp #twitch
      </div>
      <div class="mt-2.5 flex flex-col">
        <div
          class="relative min-h-[480px] max-h-[580px] w-full flex items-center cursor-pointer"
        >
          <iframe
            v-bind:src="Url"
            frameborder="0"
            allowfullscreen="true"
            scrolling="no"
            height="480"
            width="665"
          ></iframe>
          <img
            class="absolute right-5 top-5"
            width="90"
            src="assets\images\shotAirLogo.svg"
          />
        </div>
        <div class="flex flex-row">
          <div class="pt-4 pr-4 text-center flex flex-col">
            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
              <Icon
                name="mdi:heart"
                size="25"
                :color="isLiked ? '#F02C56' : ''"
              />
            </button>
            <span class="text-xs text-gray-800 font-semibold pt-2">43</span>
          </div>
          <div class="pt-4 pr-4 text-center flex flex-col">
            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
              <Icon
                name="ri:share-forward-fill"
                size="25"
                :color="isLiked ? '#F02C56' : ''"
              />
            </button>
            <span class="text-xs text-gray-800 font-semibold pt-2">43</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const a = new URL(
  "https://www.twitch.tv/parisplatynov/clip/BenevolentEntertainingKuduOMGScoots-vK7pxv7JegP1hOU1?a=2"
);
const saplitedPathname = a.pathname.split("/");
const clipID = a.pathname.split("/")[saplitedPathname.length - 1];
const Url = `https://clips.twitch.tv/embed?clip=${clipID}&parent=localhost`;

clipUrl: Url;
</script>
