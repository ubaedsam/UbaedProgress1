<template>
  <div class="lg:w-full xl:w-1/3">
              <div class="relative block bg-white rounded-lg shadow-lg">
                      <div class="flex">
                        <div
                          class="relative overflow-hidden bg-no-repeat bg-cover relative overflow-hidden bg-no-repeat bg-cover shadow-lg rounded-lg mx-4 -mt-4"
                          data-mdb-ripple="true" data-mdb-ripple-color="light">
                          <img :src="product.thumbnail" width="600px" height="400px" />
                          <a href="#!">
                            <div
                              class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed opacity-0 hover:opacity-100 transition duration-300 ease-in-out"
                              style="background-color: rgba(251, 251, 251, 0.15)"></div>
                          </a>
                        </div>
                      </div>
                      <div class="p-6">
                        <div class="flex justify-between mb-2">
                          <h5 class="font-bold text-lg">{{ product.title }}</h5>
                          <span><ul class="flex justify-center">
                            <li>
                              <svg
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 24 24"
                                fill="currentColor"
                                class="mr-1 h-5 w-5 text-warning">
                                <path
                                  fill-rule="evenodd"
                                  d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.007 5.404.433c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.433 2.082-5.006z"
                                  clip-rule="evenodd" />
                              </svg>
                            </li>
                            <li>
                              {{ product.rating }}
                            </li>
                          </ul></span>
                        </div>
                        <p class="text-gray-500 mb-2">{{ product.brand }}</p>
                        <p class="text-gray-500 mb-2">
                          {{ product.category }}
                        </p>
                        <p class="font-bold text-lg mb-4">${{ product.price }} <span class="font-normal text-gray-500"></span></p>
                        <nuxt-link class="inline-block px-7 py-3 mr-2 bg-orange-500 text-white font-medium text-sm leading-snug uppercase rounded-lg shadow-md hover:bg-rose-700 hover:shadow-lg focus:bg-rose-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-rose-800 active:shadow-lg transition duration-150 ease-in-out" data-mdb-ripple="true" data-mdb-ripple-color="light" :to="'/product/'+product.id" role="button">Detail Product</nuxt-link>
                      </div>
              </div>
            </div>
</template>

<script>
export default{
  props: ['product']
}
</script>

<style>
</style>