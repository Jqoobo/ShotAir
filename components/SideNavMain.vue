<template>
  <div 
        id="SideNavMain" 
        :class="route.fullPath === '/' ? 'lg:w-[310px]' : 'lg:w-[220px]'" 
        class="fixed z-20 bg-[#121212] pt-[85px] h-full lg:border-r-0 border-r w-[75px] overflow-auto"
    >
    <div class="lg:w-full w-[55px] mx-auto text-white">
        <NuxtLink to="/">
            <MenuItem iconString="Dla Ciebie" colorString="#16dbff" sizeString="30"/>
            </NuxtLink>
            <MenuItem iconString="Obserwowane" colorString="#FFF" sizeString="27"/>
            <MenuItem iconString="Na żywo" colorString="#FFF" sizeString="27"/>
            <div class="border-b lg:ml-2 mt-2" />
            <div class="lg:block hidden text-xs text-gray-400 font-semibold pt-4 pb-2 px-2">
                Proponowani twórcy
            </div>
            <div class="lg:hidden block pt-3" />

            <div  class="cursor-pointer">
                <MenuItemFollow/>
                </div>             
    </div>
    <button class="lg:block hidden text-[#16dbff] pt-1.5 pl-2 text-[13px]">Zobacz wszystkich</button>
    <div class="border-b lg:ml-2 mt-2" />
    <div class="lg:block hidden text-xs text-gray-400 font-semibold pt-4 pb-2 px-2">
                Obserwowane
            </div>
            <div class="lg:hidden block pt-3" />

            <div  class="cursor-pointer">
                <MenuItemFollow/>
                </div>             
    <button class="lg:block hidden text-[#16dbff] pt-1.5 pl-2 text-[13px]">Zobacz więcej</button>
    <div class="border-b lg:ml-2 mt-2" />
    <div class="lg:block hidden text-[11px] text-gray-400">
                <div class="pt-4 px-2">O ShotAir</div>
                <div class="pt-4 px-2">Kontakt</div>
                <div class="pt-4 px-2">Polityka prywatności</div>
                <div class="pt-4 px-2">© 2023 ShotAir</div>
            </div>
            <div class="pb-14"></div>
            
</div>

</template>

<script setup>
const route = useRoute()

</script>

