<template>
  <a href="/kuba">
    <div
      class="flex items-center hover:bg-[#ebebeb] rounded-md w-full py-1.5 px-2"
    >
      <img
        class="rounded-full lg:mx-0 mx-auto"
        width="35"
        src="assets\images\balenciaga3.png"
      />
      <div class="lg:pl-2.5 lg:block hidden">
        <div class="flex items-center">
          <div class="font-bold text-[14px] text-black">Kuba</div>
          <div class="ml-1 rounded-full bg-[#16dbff] h-[14px] relative">
            <Icon
              class="relative -top-[7px]"
              name="teenyicons:tick-small-solid"
              color="#FFFFFF"
              size="15"
            />
          </div>
        </div>
        <div class="font-light text-[12px] text-gray-400">@kuba_rzz</div>
      </div>
    </div>
  </a>
  <a href="/kacper">
    <div
      class="flex items-center hover:bg-[#ebebeb] rounded-md w-full py-1.5 px-2"
    >
      <img
        class="rounded-full lg:mx-0 mx-auto"
        width="35"
        src="assets\images\balenciaga1.png"
      />
      <div class="lg:pl-2.5 lg:block hidden">
        <div class="flex items-center">
          <div class="font-bold text-[14px] text-black">Kacper</div>
          <div class="ml-1 rounded-full bg-[#16dbff] h-[14px] relative">
            <Icon
              class="relative -top-[7px]"
              name="teenyicons:tick-small-solid"
              color="#FFFFFF"
              size="15"
            />
          </div>
        </div>
        <div class="font-light text-[12px] text-gray-400">@kacperlol</div>
      </div>
    </div>
  </a>
  <a href="/michal">
    <div
      class="flex items-center hover:bg-[#ebebeb] rounded-md w-full py-1.5 px-2"
    >
      <img
        class="rounded-full lg:mx-0 mx-auto"
        width="35"
        src="assets/images/balenciaga4.png"
      />
      <div class="lg:pl-2.5 lg:block hidden">
        <div class="flex items-center">
          <div class="font-bold text-[14px] text-black">Michał</div>
          <div class="ml-1 rounded-full bg-[#16dbff] h-[14px] relative">
            <Icon
              class="relative -top-[7px]"
              name="teenyicons:tick-small-solid"
              color="#FFFFFF"
              size="15"
            />
          </div>
        </div>
        <div class="font-light text-[12px] text-gray-400">@pu0238</div>
      </div>
    </div>
  </a>
  <a href="/konrad">
    <div
      class="flex items-center hover:bg-[#ebebeb] rounded-md w-full py-1.5 px-2"
    >
      <img
        class="rounded-full lg:mx-0 mx-auto"
        width="35"
        src="assets/images/balenciaga2.png"
      />
      <div class="lg:pl-2.5 lg:block hidden">
        <div class="flex items-center">
          <div class="font-bold text-[14px] text-black">Konrad</div>
          <div class="ml-1 rounded-full bg-[#16dbff] h-[14px] relative">
            <Icon
              class="relative -top-[7px]"
              name="teenyicons:tick-small-solid"
              color="#FFFFFF"
              size="15"
            />
          </div>
        </div>
        <div class="font-light text-[12px] text-gray-400">@darnok</div>
      </div>
    </div>
  </a>
</template>

<script setup>
defineProps(["user"]);
</script>
