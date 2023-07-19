<template>
  <div
    id="TopNav"
    class="fixed bg-black z-30 flex items-center w-full h-[75px]"
  >
    <div class="flex items-center justify-between w-full px-6 mx-auto">
      <div :class="route.fullPath === '/' ? 'w-[80%]' : 'lg:w-[20%] w-[70%]'">
        <NuxtLink to="/">
          <img width="145" src="assets\images\shotAirLogo.svg" alt="logo" />
        </NuxtLink>
      </div>
      <div
        class="flex items-center justify-end gap-3 min-w-[275px] max-w-[320px] w-full"
      >
        <a href="/upload" v-if="upload">
          <button
            class="flex items-center rounded-sm px-3 py-[6px] bg-[#ff7f50]"
          >
            <Icon name="mdi:plus" color="#FFF" size="22" />
            <span class="text-white px-2 font-medium text-[15px]">Dodaj</span>
          </button>
        </a>

        <div v-if="true" class="flex items-center">
          <a href="/logowanie">
            <button
              class="flex items-center bg-[#16dbff] text-black rounded-md px-3 py-[8px]"
              v-if="logIn"
            >
              <span class="mx-4 font-medium text-[15px]">Zaloguj się</span>
            </button>
          </a>
        </div>
        <div class="flex items-center">
          <div class="relative">
            <button
              class="mt-1"
              v-if="profilePic"
              @click="($event) => (showMenu = !showMenu)"
            >
              <img
                class="rounded-full"
                width="33"
                src="assets\images\balenciaga3.png"
              />
            </button>
            <div
              v-if="showMenu"
              id="PopupMenu"
              class="absolute bg-white rounded-lg py-1.5 w-[200px] shadow-xl top-[43px] -right-2 border border-gray-300"
            >
              <div
                class="flex items-center justify-start py-3 px-2 hover:bg-[#ebebeb] cursor-pointer"
                @click="logOut"
              >
                <Icon name="ic:outline-login" size="20" />
                <span class="pl-2 font-semibold text-sm">Wyloguj się</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    const route = useRoute();
    let showMenu = ref(false);
    return {
      route,
      showMenu,
    };
  },
  data() {
    return {
      showMenu: false,
      profilePic: false,
      logIn: true,
      upload: false,
    };
  },
  methods: {
    async logOut() {
      localStorage.removeItem("access_token");
      this.profilePic = false;
      this.logIn = true;
      this.upload = false;
      window.location.reload();
    },
  },
  async mounted() {
    const token = localStorage.getItem("access_token");
    console.log(token);
    if (token) {
      this.profilePic = true;
      this.logIn = false;
      this.upload = true;
    }
  },
};
</script>
