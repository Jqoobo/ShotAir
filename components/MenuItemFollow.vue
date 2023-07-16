<template>
    <div class="flex items-center hover:bg-[#303030] rounded-md w-full py-1.5 px-2">
        <img 
            class="rounded-full lg:mx-0 mx-auto" 
            width="35" 
            src="assets\images\c635b669d116b4da3e9fa3f29517d41d.jpg"
        >
        <div class="lg:pl-2.5 lg:block hidden">
            <div class="flex items-center">
                <div class="font-bold text-[14px] text-white">
                    Nazwa użytkownika
                </div>
                <div class="ml-1 rounded-full bg-[#ff7f50] h-[14px] relative">
                    <Icon class="relative -top-[7px]" name="teenyicons:tick-small-solid" color="#FFFFFF" size="15"/>
                </div>
            </div>
            <div class="font-light text-[12px] text-gray-400">
                Nazwa użytkownika
            </div>
        </div>
    </div>
</template>

<script setup>
defineProps(['user'])
</script>
