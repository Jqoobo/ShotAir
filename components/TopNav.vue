<template>
  <div
      id="TopNav"
      class="fixed bg-[#121212] z-30 flex items-center w-full border-b h-[75px]"
  >
  <div
    :class="route.fullPath === '/' ? 'max-w-[1150px]' : ''"
    class="flex items-center justify-between w-full px-6 mx-auto"
    >
    <div
        :class="route.fullPath === '/' ? 'w-[80%]' : 'lg:w-[20%] w-[70%]'"
        >
        <NuxtLink to="/">
         <img width="145" src="assets\images\shotAirLogo.svg" alt="logo" />
        </NuxtLink>
  </div>
  <div
  class="hidden md:flex items-center  bg-[#303030] p-1 rounded-full max-w-[380px] w-full"
  >
  <input
  type="text"
  class="w-full pl-3 my-2 placeholder-[#838383] text-[15px] text-white focus:outline-none bg-transparent"
  placeholder="Wyszukaj twórców"
  > 
  <div
  class="px-3 py-1 flex items-center border-l border-l-gray-300"
  >
  <Icon name="ri:search-line" color="#FFF" size="22"/>
  </div>
  </div>
  <div class="flex items-center justify-end gap-3 min-w-[275px] max-w-[320px] w-full"> 
  <button class="flex items-center rounded-sm px-3 py-[6px] bg-[#ff7f50]">
    <Icon name="mdi:plus" color="#FFF" size="22"/>
    <span class="text-white px-2 font-medium text-[15px]">Dodaj</span>
  </button>

  <div v-if="false" class="flex items-center">
    <button class="flex items-center bg-[#16dbff] text-black rounded-md px-3 py-[8px]">
      <span class="mx-4 font-medium text-[15px]">Zaloguj się</span>
    </button> 
    <Icon name="mdi:dots-vertical" color="#FFF" size="25"/>
  </div>
  <div class="flex items-center"> 
    <Icon class="ml-1 mr-4" name="carbon:send-alt" color="#FFF" size="30"/>
    <Icon class="mr-5" name="bx:message-detail" color="#FFF" size="27"/>
   <div class="relative"> 
   <button 
   class="mt-1"
   @click="$event => showMenu = !showMenu"
   >
    <img
    class="rounded-full"
    width="33"
    src="assets\images\c635b669d116b4da3e9fa3f29517d41d.jpg"
    >
   </button>
   <div
   v-if="showMenu"
id="PopupMenu"
class="absolute bg-[#ebebeb] rounded-lg py-1.5 w-[200px] shadow-xl top-[43px] -right-2 border border-gray-300"
   >
<NuxtLink 
@click="$event => showMenu = false" 
class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 cursor-pointer">
<Icon name="ph:user" size="20"/>
<span class="pl-2 font-semibold text-sm">Profil</span>
</NuxtLink>
<div
class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 border-t cursor-pointer">
<Icon name="ic:outline-login" size="20"/>
<span class="pl-2 font-semibold text-sm">Wyloguj się</span>
</div>
   </div>
   </div>
  </div>
  </div>
  </div>
  </div>
</template>

<script setup>
const route = useRoute()
let showMenu = ref(false)

</script>

