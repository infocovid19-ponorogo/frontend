<template>
  <nav class="w-full fixed bg-blue-400 lg:p-6 shadow-xs">
    <div class="container lg:mx-auto">
      <div class="flex">
        <div class="max-w-sm flex items-center flex-shrink-0 text-white mr-6 lg:p-0 pl-6 py-2">
          <img
            class="lg:fill-current h-10 lg:h-16 lg:w-full"
            src="~/assets/icon.svg"
            alt="infocovid19ponorogo.id"
          />
        </div>
        <div class="lg:relative fixed bottom-0 w-full bg-blue-400 h-14 py-2 lg:pt-4">
          <ul class="flex flex-row lg:justify-start justify-between text-center ml-3">
            <li class="flex-1 lg:flex-none mr-2">
              <nuxt-link to="/" :class="activeLink('/')">
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5 fill-current"
                    v-bind:class="isActiveLink('/') ? 'text-white' : 'text-black'"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="15"
                    height="15"
                  >
                    <path
                      class="heroicon-ui"
                      d="M13 20v-5h-2v5a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2v-7.59l-.3.3a1 1 0 1 1-1.4-1.42l9-9a1 1 0 0 1 1.4 0l9 9a1 1 0 0 1-1.4 1.42l-.3-.3V20a2 2 0 0 1-2 2h-3a2 2 0 0 1-2-2zm5 0v-9.59l-6-6-6 6V20h3v-5c0-1.1.9-2 2-2h2a2 2 0 0 1 2 2v5h3z"
                    />
                  </svg>
                </div>
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Beranda</span>
              </nuxt-link>
            </li>
            <li class="flex-1 lg:flex-none mr-2">
              <nuxt-link to="/info" :class="activeLink('/info')">
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5 fill-current"
                    v-bind:class="isActiveLink('/info') ? 'text-white' : 'text-black'"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="15"
                    height="15"
                  >
                    <path
                      class="heroicon-ui"
                      d="M12 22a10 10 0 1 1 0-20 10 10 0 0 1 0 20zm0-2a8 8 0 1 0 0-16 8 8 0 0 0 0 16zm0-9a1 1 0 0 1 1 1v4a1 1 0 0 1-2 0v-4a1 1 0 0 1 1-1zm0-4a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"
                    />
                  </svg>
                </div>
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Informasi</span>
              </nuxt-link>
            </li>
            <li class="flex-1 lg:flex-none mr-2">
              <nuxt-link to="/about-us" :class="activeLink('/about-us')">
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5 fill-current"
                    v-bind:class="isActiveLink('/about-us') ? 'text-white' : 'text-black'"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="15"
                    height="15"
                  >
                    <path
                      class="heroicon-ui"
                      d="M4 15a3 3 0 1 1 0-6 3 3 0 0 1 0 6zm0-2a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm8 2a3 3 0 1 1 0-6 3 3 0 0 1 0 6zm0-2a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm8 2a3 3 0 1 1 0-6 3 3 0 0 1 0 6zm0-2a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"
                    />
                  </svg>
                </div>
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Tentang Kami</span>
              </nuxt-link>
            </li>
            <li class="flex-1 lg:flex-none mr-2">
              <nuxt-link to="/policy-privacy" :class="activeLink('/policy-privacy')">
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5 fill-current"
                    v-bind:class="isActiveLink('/policy-privacy') ? 'text-white' : 'text-black'"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="15"
                    height="15"
                  >
                    <path
                      class="heroicon-ui"
                      d="M7 10V7a5 5 0 1 1 10 0v3h2a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-8c0-1.1.9-2 2-2h2zm2 0h6V7a3 3 0 0 0-6 0v3zm-4 2v8h14v-8H5zm7 2a1 1 0 0 1 1 1v2a1 1 0 0 1-2 0v-2a1 1 0 0 1 1-1z"
                    />
                  </svg>
                </div>
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Kebijakan Privasi</span>
              </nuxt-link>
            </li>
            <li class="flex-1 lg:flex-none mr-2">
              <nuxt-link to="/pernyataan-resmi" :class="activeLink('/pernyataan-resmi')">
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5 fill-current"
                    v-bind:class="isActiveLink('/pernyataan-resmi') ? 'text-white' : 'text-black'"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="15"
                    height="15"
                  >
                    <path
                      class="heroicon-ui"
                      d="M6 2h9a1 1 0 0 1 .7.3l4 4a1 1 0 0 1 .3.7v13a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V4c0-1.1.9-2 2-2zm9 2.41V7h2.59L15 4.41zM18 9h-3a2 2 0 0 1-2-2V4H6v16h12V9z"
                    />
                  </svg>
                </div>
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Pernyataan Resmi</span>
              </nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    activeLink(link) {
      let isActive = this.isActiveLink(link);
      return isActive
        ? "flex flex-col text-white lg:border-b-2 lg:border-white lg:pb-2 lg:mr-5"
        : "flex flex-col lg:border-b-2 lg:border-gray-400 lg:border-none lg:pb-2 lg:mr-5";
    },
    isActiveLink(link) {
      let firtspath = this.$route.path.split("/")[1];
      return link == "/" + firtspath;
    }
  }
};
</script>

<style>
.text-super-xs {
  font-size: 8.1px;
}
@media (min-width: 1024px) {
  .text-super-xs {
      font-size: 1rem;
  }
}
</style>
