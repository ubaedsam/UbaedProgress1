<template>
<!-- Container for demo purpose -->
<div class="container my-24 px-6 mx-auto">

<!-- Section: Design Block -->
<section class="mb-20 text-gray-800 text-center">

  <h2 class="text-3xl font-bold mb-12 pb-4 text-center">Types of products</h2>

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

        <searchIndex></searchIndex>
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

  <div class="grid sm:grid-cols-3 md:grid-cols-3 lg:grid-cols-3 gap-8 xl:gap-x-12">
    <div class="mb-6 lg:mb-0">
      <div class="relative block bg-white rounded-lg shadow-lg">
        <div class="flex">
          <div
            class="relative overflow-hidden bg-no-repeat bg-cover relative overflow-hidden bg-no-repeat bg-cover shadow-lg rounded-lg mx-4 -mt-4"
            data-mdb-ripple="true" data-mdb-ripple-color="light">
            <img src="https://source.unsplash.com/600x400?fast food" class="w-full" />
            <a href="#!">
              <div
                class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed opacity-0 hover:opacity-100 transition duration-300 ease-in-out"
                style="background-color: rgba(251, 251, 251, 0.15)"></div>
            </a>
          </div>
        </div>
        <div class="p-6">
          <h5 class="font-bold text-2xl text-lg mb-3">Fast Food</h5>
        </div>
      </div>
    </div>

    <div class="mb-6 lg:mb-0">
      <div class="relative block bg-white rounded-lg shadow-lg">
        <div class="flex">
          <div
            class="relative overflow-hidden bg-no-repeat bg-cover relative overflow-hidden bg-no-repeat bg-cover shadow-lg rounded-lg mx-4 -mt-4"
            data-mdb-ripple="true" data-mdb-ripple-color="light">
            <img src="https://source.unsplash.com/600x400?food" class="w-full" />
            <a href="#!">
              <div
                class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed opacity-0 hover:opacity-100 transition duration-300 ease-in-out"
                style="background-color: rgba(251, 251, 251, 0.15)"></div>
            </a>
          </div>
        </div>
        <div class="p-6">
          <h5 class="font-bold text-2xl text-lg mb-3">Food</h5>
        </div>
      </div>
    </div>

    <div class="mb-0">
      <div class="relative block bg-white rounded-lg shadow-lg">
        <div class="flex">
          <div
            class="relative overflow-hidden bg-no-repeat bg-cover relative overflow-hidden bg-no-repeat bg-cover shadow-lg rounded-lg mx-4 -mt-4"
            data-mdb-ripple="true" data-mdb-ripple-color="light">
            <img src="https://source.unsplash.com/600x400?drink" class="w-full" />
            <a href="#!">
              <div
                class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed opacity-0 hover:opacity-100 transition duration-300 ease-in-out"
                style="background-color: rgba(251, 251, 251, 0.15)"></div>
            </a>
          </div>
        </div>
        <div class="p-6">
          <h5 class="font-bold text-2xl text-lg mb-3">Drink</h5>
        </div>
      </div>
    </div>

    <div class="mb-6 lg:mb-0">
      <div class="relative block bg-white rounded-lg shadow-lg">
        <div class="flex">
          <div
            class="relative overflow-hidden bg-no-repeat bg-cover relative overflow-hidden bg-no-repeat bg-cover shadow-lg rounded-lg mx-4 -mt-4"
            data-mdb-ripple="true" data-mdb-ripple-color="light">
            <img src="https://source.unsplash.com/600x400?cake" class="w-full" />
            <a href="#!">
              <div
                class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed opacity-0 hover:opacity-100 transition duration-300 ease-in-out"
                style="background-color: rgba(251, 251, 251, 0.15)"></div>
            </a>
          </div>
        </div>
        <div class="p-6">
          <h5 class="font-bold text-2xl text-lg mb-3">Cake</h5>
        </div>
      </div>
    </div>

    <div class="mb-6 lg:mb-0">
      <div class="relative block bg-white rounded-lg shadow-lg">
        <div class="flex">
          <div
            class="relative overflow-hidden bg-no-repeat bg-cover relative overflow-hidden bg-no-repeat bg-cover shadow-lg rounded-lg mx-4 -mt-4"
            data-mdb-ripple="true" data-mdb-ripple-color="light">
            <img src="https://source.unsplash.com/600x400?snack" class="w-full" />
            <a href="#!">
              <div
                class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed opacity-0 hover:opacity-100 transition duration-300 ease-in-out"
                style="background-color: rgba(251, 251, 251, 0.15)"></div>
            </a>
          </div>
        </div>
        <div class="p-6">
          <h5 class="font-bold text-lg text-2xl mb-3">Snack</h5>
        </div>
      </div>
    </div>

    <div class="mb-0">
      <div class="relative block bg-white rounded-lg shadow-lg">
        <div class="flex">
          <div
            class="relative overflow-hidden bg-no-repeat bg-cover relative overflow-hidden bg-no-repeat bg-cover shadow-lg rounded-lg mx-4 -mt-4"
            data-mdb-ripple="true" data-mdb-ripple-color="light">
            <img src="https://source.unsplash.com/600x400?cake" class="w-full" />
            <a href="#!">
              <div
                class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed opacity-0 hover:opacity-100 transition duration-300 ease-in-out"
                style="background-color: rgba(251, 251, 251, 0.15)"></div>
            </a>
          </div>
        </div>
        <div class="p-6">
          <h5 class="font-bold text-lg text-2xl mb-3">Traditional Cake</h5>
        </div>
      </div>
    </div>
  </div>

</section>
<!-- Section: Design Block -->

</div>
<!-- Container for demo purpose -->
</template>

<style>
body {
  background-color: hsl(0, 0%, 97%)
}
</style>

<!-- <script>
export default{
  data(){
    return {
      data: [],
    };
  },
  components:{

  },
  methods: {
    async fetchData(){
      const response = await fetch('https://dummyjson.com/products/categories');
      this.data = await response.json();
      const data = this.data;
      console.log(data[0])
      return data;
    },
  },
  async mounted(){
    this.category = await this.fetchData();
  }
}
</script> -->

<!-- <script setup>
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
</script> -->