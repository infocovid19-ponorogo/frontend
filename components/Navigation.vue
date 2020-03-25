<template>
  <nav class="w-full fixed bg-blue-400 lg:p-6 shadow-xs">
    <div class="container lg:mx-auto">
      <div class="flex">
        <div class="max-w-sm flex items-center flex-shrink-0 text-white mr-6 lg:p-0 p-6">
          <img class="lg:fill-current h-10 lg:h-16 lg:w-full" src="~/assets/icon.svg" alt="">
        </div>
        <div class="lg:relative fixed bottom-0 w-full bg-blue-400 h-16 pt-2">
          <ul class="flex flex-row lg:justify-start justify-between text-center ml-3">
            <li class="flex-1 lg:flex-none ml-3 mr-3">
              <a href class="flex flex-col border-b-2 border-white lg:pb-2 lg:mr-5">
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="18"
                    height="18"
                  >
                    <path
                      class="heroicon-ui"
                      d="M13 20v-5h-2v5a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2v-7.59l-.3.3a1 1 0 1 1-1.4-1.42l9-9a1 1 0 0 1 1.4 0l9 9a1 1 0 0 1-1.4 1.42l-.3-.3V20a2 2 0 0 1-2 2h-3a2 2 0 0 1-2-2zm5 0v-9.59l-6-6-6 6V20h3v-5c0-1.1.9-2 2-2h2a2 2 0 0 1 2 2v5h3z"
                    />
                  </svg>
                </div>
                <span class="lg:text-base text-xs text-white py-1">Beranda</span>
              </a>
            </li>
            <li class="flex-1 lg:flex-none mr-3">
              <a
                href
                class="flex flex-col border-b-2 border-gray-400 lg:border-none lg:pb-2 lg:mr-5"
              >
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="18"
                    height="18"
                  >
                    <path
                      class="heroicon-ui"
                      d="M12 22a10 10 0 1 1 0-20 10 10 0 0 1 0 20zm0-2a8 8 0 1 0 0-16 8 8 0 0 0 0 16zm0-9a1 1 0 0 1 1 1v4a1 1 0 0 1-2 0v-4a1 1 0 0 1 1-1zm0-4a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"
                    />
                  </svg>
                </div>
                <span class="lg:text-base text-xs text-gray-800 lg:text-white py-1">Informasi</span>
              </a>
            </li>
            <li class="flex-1 lg:flex-none mr-3">
              <a
                href
                class="flex flex-col border-b-2 border-gray-400 lg:border-none lg:pb-2 lg:mr-5"
              >
                <div class="flex justify-center">
                  <svg
                    class="lg:hidden w-5"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    width="18"
                    height="18"
                  >
                    <path
                      class="heroicon-ui"
                      d="M4 15a3 3 0 1 1 0-6 3 3 0 0 1 0 6zm0-2a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm8 2a3 3 0 1 1 0-6 3 3 0 0 1 0 6zm0-2a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm8 2a3 3 0 1 1 0-6 3 3 0 0 1 0 6zm0-2a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"
                    />
                  </svg>
                </div>
                <a href="about-us" class="lg:text-base text-xs text-gray-800 lg:text-white py-1">Tentang Kami</a>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style>
</style>
