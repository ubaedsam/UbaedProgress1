<template>
<div
    class="relative overflow-hidden bg-cover bg-no-repeat shadow-lg"
    style="
      background-position: 50%;
      background-image: url('https://source.unsplash.com/random?store');
      height: 400px;
    ">
    <div
      class="absolute bottom-0 left-0 right-0 top-0 h-full w-full overflow-hidden bg-fixed"
      style="background-color: rgba(0, 0, 0, 0.75)">
      <div class="flex h-full items-center justify-center">
        <div class="px-6 text-center text-white md:px-12">
            <img src="/websiteku.png" width="133px" class="mb-5">
            <NuxtLink
            type="button"
            class="inline-block rounded border-2 border-neutral-50 px-6 pb-[6px] pt-2 text-xs font-medium uppercase leading-normal text-neutral-50 transition duration-150 ease-in-out hover:border-neutral-100 hover:bg-neutral-500 hover:bg-opacity-10 hover:text-neutral-100 focus:border-neutral-100 focus:text-neutral-100 focus:outline-none focus:ring-0 active:border-neutral-200 active:text-neutral-200 dark:hover:bg-neutral-100 dark:hover:bg-opacity-10"
            data-te-ripple-init
            data-te-ripple-color="light" to="/product" role="button">
            All Product
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>