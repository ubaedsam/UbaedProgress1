<template>
    <div class="container my-20 px-6 mx-auto">
      <h2 class="text-3xl font-bold mb-4">Products</h2>
      <p class="mb-7 text-gray-500">
        this is the best product from our store please try it guaranteed you won't regret it
      </p>
      <section class="text-gray-800">

        <h1 class="lg:text-lg font-medium mb-5">
						Filter Category
						<button
							v-if="activeCategory"
							@click="setCategory(null)"
							class="px-3 rounded-sm text-[13px] capitalize bg-gray-200 ml-5"
						>
							Clear &times;
						</button>
					</h1>
					<div class="flex flex-wrap l items-center lg:space-x-5 mb-5">
						<template v-for="(c, i) in categories" :key="`categroy-${i}`">
							<button
								@click="setCategory(c)"
								:class="{
									'bg-primary-100 text-primary': c == activeCategory,
									' bg-gray-200': c !== activeCategory,
								}"
								class="px-3 py-2 rounded-sm text-[13px] capitalize shrink-0 mr-4 mb-4 lg:mr-0 lg:mb-0"
							>
								{{ c }}
							</button>
						</template>
					</div>
        <div class="flex flex-wrap grid sm:container xs:grid-cols-3 sm:grid-cols-3 md:grid-cols-3 lg:grid-cols-3 gap-8 xl:gap-x-12">
          <template
							v-for="(p, i) in filterProducts"
							:key="`product-${i}-${p.id}`"
						>
            <div id="default-carousel" class="relative w-full h-full" data-carousel="slide">
            <div class="relative h-56 overflow-hidden rounded-lg">
                    <img :src="p.thumbnail"
									:alt="p.title" class="absolute block w-full h-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2">
            </div>
            <div class="mt-4">
              <div class="flex justify-between">
                          <p class="font-bold text-lg">{{ p.title }}</p>
                          <span><ul class="flex justify-center">
                            <li>
                              <svg
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 24 24"
                                fill="currentColor"
                                class="mr-1 mt-0 h-5 w-5 text-warning">
                                <path
                                  fill-rule="evenodd"
                                  d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.007 5.404.433c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.433 2.082-5.006z"
                                  clip-rule="evenodd" />
                              </svg>
                            </li>
                            <li>
                              {{ p.rating }}
                            </li>
                          </ul></span>
            </div>
            <p class="text-gray-500">{{ p.brand }}</p>
                        <p class="text-gray-500 mb-3">
                          {{ p.category }}
                        </p>
                        <p class="font-bold text-lg mb-4">{{ formatPrice(p.price) }} <span class="font-normal text-gray-500"></span></p>
                        <NuxtLink class="inline-block px-7 py-3 mr-2 bg-orange-500 text-white font-medium text-sm leading-snug uppercase rounded-lg shadow-md hover:bg-rose-700 hover:shadow-lg focus:bg-rose-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-rose-800 active:shadow-lg transition duration-150 ease-in-out" data-mdb-ripple="true" data-mdb-ripple-color="light" :to="'/product/' + p.id" role="button">Detail Product</NuxtLink>
            </div>
            </div>
          </template>
        </div>

      </section>

      <!-- <section class="lg:px-[15%] px-[5%] pt-20">
				<h1
					class="lg:text-5xl text-2xl leading-normal font-semibold text-center"
				>
					Stay Up To Date With The
				</h1>
				<h1
					class="lg:text-6xl text-4xl text-center leading-normal font-bold rainbow-text"
				>
					Latest Fashion Trends
				</h1>

				<div class="lg:mt-20 mt-10">
					<h1 class="lg:text-lg font-medium mb-5">
						Filter Category
						<button
							v-if="activeCategory"
							@click="setCategory(null)"
							class="px-3 rounded-sm text-[13px] capitalize bg-gray-200 ml-5"
						>
							Clear &times;
						</button>
					</h1>
					<div class="flex flex-wrap l items-center lg:space-x-5 mb-5">
						<template v-for="(c, i) in categories" :key="`categroy-${i}`">
							<button
								@click="setCategory(c)"
								:class="{
									'bg-primary-100 text-primary': c == activeCategory,
									' bg-gray-200': c !== activeCategory,
								}"
								class="px-3 py-2 rounded-sm text-[13px] capitalize shrink-0 mr-4 mb-4 lg:mr-0 lg:mb-0"
							>
								{{ c }}
							</button>
						</template>
					</div>
					<div class="grid grid-cols-1 lg:grid-cols-4 gap-10 lg:mt-20">
						<template
							v-for="(p, i) in filterProducts"
							:key="`product-${i}-${p.id}`"
						>
								<img
									:src="p.thumbnail"
									:alt="p.title"
									class="w-full h-[300px] object-contain object-center"
								/>
								<div class="p-3">
									<h2 class="text-xs">{{ p.title }}</h2>
									<p class="font-bold text-sm mt-2">
										{{ formatPrice(p.price) }}
									</p>
								</div>
						</template>
					</div>
				</div>
	    </section> -->
    </div>
</template>
    
<!-- <script setup>
import { onMounted } from 'vue'
import { 
    initAccordions, 
    initCarousels, 
    initCollapses, 
    initDials, 
    initDismisses, 
    initDrawers, 
    initDropdowns, 
    initModals, 
    initPopovers, 
    initTabs, 
    initTooltips } from 'flowbite'

// initialize components based on data attribute selectors
onMounted(() => {
    initAccordions();
    initCarousels();
    initCollapses();
    initDials();
    initDismisses();
    initDrawers();
    initDropdowns();
    initModals();
    initPopovers();
    initTabs();
    initTooltips();
})

const {pending, data: count} = await useFetch('https://dummyjson.com/products', {
  lazy: true
})
</script> -->

<script setup>
	const { data: products } = await useAsyncData("products", () => {
		return queryContent("merch").find();
	});

	// create an array of categories from the products
	const categories = products.value[0].body.reduce((acc, product) => {
		if (!acc.includes(product.category)) {
			acc.push(product.category);
		}
		return acc;
	}, []);

	//var used to store the active category
	const activeCategory = ref(null);

	// function used to set the active category
	const setCategory = (category) => {
		activeCategory.value = category;
		useRouter().push({
			query: {
				category: category,
			},
		});
	};
	// set category on mount if it exist in query
	onMounted(() => {
		if (useRoute().query.category) {
			activeCategory.value = useRoute().query.category;
		}
	});

	// function used to format the price
	const formatPrice = (price) => {
		return new Intl.NumberFormat("en-US", {
			style: "currency",
			currency: "USD",
		}).format(price);
	};

	// function used to filter the products by category
	const filterProducts = computed(() => {
		if (!activeCategory.value) {
			return products.value[0].body;
		}
		return products.value[0].body.filter((product) => {
			return (
				product.category.toLowerCase() == activeCategory.value.toLowerCase()
			);
		});
	});

	// Set header
	useHead({
		title: "Content Merch",
	});
</script>

<style scoped>
  body {
    background-color: hsl(0, 0%, 97%)
  }
</style>

<!-- <script setup>
const runTimeConfig = useRuntimeConfig();

const products = ref([])
onMounted(()=>{
  fetch(`${runTimeConfig.public.baseUrl}/products`, {
    headers: {
      Authorization: `Bearer ${runTimeConfig.public.appSecret}`,
    },
  }).then(res => res.json()).then(data => products.value = data);
});
</script> -->

<!-- <script setup>

const runtimeConfigs = useRuntimeConfig()
const page = ref(1)

const {data: products, pending, refresh} = await useFetch(()=>`${runtimeConfigs.public.API_URL}/products?page=${page.value}`, {
    key: `productlist-${page.value}`,
})

function refetch(pageNumber){
    page.value = pageNumber
    refresh()
}

</script> -->

<!-- <script setup>
const { data: products } = await useFetch('https://dummyjson.com/products?limit=12')
</script> -->