<template>
   <div id="PostMain" class="flex border-b py-6">
    <div class="cursor-pointer">
            <img class="rounded-full max-h-[60px]" width="60" src="assets\images\c635b669d116b4da3e9fa3f29517d41d.jpg">
        </div>
        <div class="pl-3 w-full px-4">
            <div class="flex items-center justify-between pb-0.5">
                <button>
                    <span class="font-bold hover:underline cursor-pointer">
                        Nazwa użytkownika
                    </span>
                    <span class="text-[13px] text-light text-gray-500 pl-1 cursor-pointer">
                        Nazwa
                    </span>
                </button>
                <button class="border text-[15px] px-[21px] py-0.5 border-[#ff7f50] text-[#ff7f50] hover:bg-[#ffeef2] font-semibold rounded-md">
                    Obserwuj
                </button>
            </div>
            <div class="text-[15px] pb-0.5 break-words md:max-w-[400px] max-w-[300px]">Test</div>
            <div class="text-[14px] text-gray-500 pb-0.5">#sky #aesthetic #mood</div>
            <div class="mt-2.5 flex">
                <div
                    class="relative min-h-[480px] max-h-[580px] w-full flex items-center bg-black rounded-xl cursor-pointer"
                >
                <video 
                        ref="video"
                        loop
                        muted
                        class="rounded-xl object-cover mx-auto h-full" 
                        src="/video.mp4" 
                    />
                    <img 
                        class="absolute right-5 top-5" 
                        width="90" 
                        src="assets\images\shotAirLogo.svg"
                    >
                    <div class="absolute bottom-0 pl-4 fle">
                        <div class="pb-4 text-center">
                            <button
                                @click="isLiked ? unlikePost(post) : likePost(post)"
                                class="rounded-full bg-[#ebebeb] p-2 cursor-pointer"
                            >
                            <Icon 
                                    name="mdi:heart" 
                                    size="25" 
                                    :color="isLiked ? '#F02C56' : ''"
                                />
                            </button>
                            <span class="text-s text-white font-semibold pl-2">43</span>
                        </div>
                        <div class="pb-4 text-center">
                            <button
                                @click="isLiked ? unlikePost(post) : likePost(post)"
                                class="rounded-full bg-[#ebebeb] p-2 cursor-pointer"
                            >
                            <Icon 
                                    name="bx:bxs-message-rounded-dots" 
                                    size="25" 
                                    :color="isLiked ? '#F02C56' : ''"
                                />
                            </button>
                            <span class="text-s text-white font-semibold pl-2">24</span>
                        </div>
                        <div class="pb-4 text-center">
                            <button
                                @click="isLiked ? unlikePost(post) : likePost(post)"
                                class="rounded-full bg-[#ebebeb] p-2 cursor-pointer"
                            >
                            <Icon 
                                    name="ri:share-forward-fill" 
                                    size="25" 
                                    :color="isLiked ? '#F02C56' : ''"
                                />
                            </button>
                            <span class="text-s text-white font-semibold pl-2">24</span>
                        </div>
                    </div>
                </div>
                    
            </div>
        </div>
        
   </div>
</template>

<script setup>

let video = ref(null)

onMounted(() => {
    video.value.play()
})

</script>

