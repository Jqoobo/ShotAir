<template>
  <div
    id="SideNavMain"
    :class="route.fullPath === '/' ? 'lg:w-[310px]' : 'lg:w-[220px]'"
    class="fixed z-20 pt-[85px] h-full lg:border-r-0 border-r w-[75px] overflow-auto"
  >
    <div class="lg:w-full w-[55px] mx-auto text-black">
      <NuxtLink to="/">
        <MenuItem iconString="Home" colorString="#ff7f50" sizeString="30" />
      </NuxtLink>
      <div class="border-b lg:ml-2 mt-2" />
      <div
        class="lg:block hidden text-xs text-gray-400 font-semibold pt-4 pb-2 px-2"
      >
        Popularni twórcy
      </div>
      <div class="lg:hidden block pt-3" />

      <div class="cursor-pointer">
        <MenuItemFollow />
      </div>
    </div>
    <div class="border-b lg:ml-2 mt-2" />
    <div class="lg:block hidden text-[11px] text-gray-400">
      <a href="/o-nas"><div class="pt-4 px-2">O ShotAir</div></a>
      <a href="/kontakt"><div class="pt-4 px-2">Kontakt</div></a>
      <a href="/polityka"><div class="pt-4 px-2">Polityka prywatności</div></a>
      <div class="pt-4 px-2">© 2023 ShotAir</div>
    </div>
    <div class="pb-14"></div>
  </div>
</template>

<script setup>
const route = useRoute();
</script>
