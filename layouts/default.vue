<template>
    <div>
    <header>
        <nav class="bg-white shadow-lg">
			<div class="max-w-8xl mx-auto px-4">
				<div class="flex justify-between">
					<div class="flex space-x-7">
						<div>
							<!-- Website Logo -->
							<NuxtLink to="/" class="flex items-center py-4 px-2">
								<img src="/websiteku.png" alt="Logo" class="h-8 w-8 mr-3 rounded-md">
								<span class="font-semibold text-gray-500 text-lg">Websiteku.id</span>
							</NuxtLink>
						</div>
						<!-- Primary Navbar items -->
						<div class="hidden md:flex items-center space-x-1">
              <NuxtLink to="/" class="halaman py-4 px-2 text-gray-500 font-semibold hover:text-orange-500 transition duration-300">Product</NuxtLink>
              <!-- <NuxtLink to="/product" class="halaman py-4 px-2 text-gray-500 font-semibold hover:text-orange-500 transition duration-300">Product</NuxtLink> -->
              <NuxtLink to="/about" class="halaman py-4 px-2 text-gray-500 font-semibold hover:text-orange-500 transition duration-300">About Us</NuxtLink>
              <NuxtLink to="/contact" class="halaman py-4 px-2 text-gray-500 font-semibold hover:text-orange-500 transition duration-300">Contact Us</NuxtLink>
              <!-- <NuxtLink to="/product/detail" class="halaman py-4 px-2 text-gray-500 font-semibold hover:text-orange-500 transition duration-300">Detail Product</NuxtLink> -->
						</div>
					</div>
					<!-- Secondary Navbar items -->
					<div class="hidden md:flex items-center space-x-3">
            <NuxtLink to="/pesanan" class="py-2 px-2 font-medium text-white bg-orange-500 rounded hover:bg-orange-400 transition duration-300">Orders : 0</NuxtLink>
						<NuxtLink to="/keranjang" class="py-2 px-2 font-medium text-gray-500 rounded hover:bg-orange-500 hover:text-white transition duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
              </svg>
            </NuxtLink>
					</div>
					<!-- Mobile menu button -->
					<div class="md:hidden flex items-center">
						<button class="outline-none mobile-menu-button">
						<svg class=" w-6 h-6 text-gray-500 hover:text-orange-500 "
							x-show="!showMenu"
							fill="none"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path d="M4 6h16M4 12h16M4 18h16"></path>
						</svg>
					</button>
					</div>
				</div>
			</div>
			<!-- mobile menu -->
			<div class="hidden mobile-menu">
				<ul class="">
          <li><NuxtLink to="/" class="block text-sm px-2 py-4 hover:bg-orange-500 transition duration-300">Product</NuxtLink></li>
					<!-- <li><NuxtLink to="/product" class="block text-sm px-2 py-4 hover:bg-orange-500 transition duration-300">Product</NuxtLink></li> -->
					<li><NuxtLink to="/about" class="block text-sm px-2 py-4 hover:bg-orange-500 transition duration-300">About Us</NuxtLink></li>
					<li><NuxtLink to="/contact" class="block text-sm px-2 py-4 hover:bg-orange-500 transition duration-300">Contact Us</NuxtLink></li>
          <li><NuxtLink to="/pesanan" class="block text-sm px-2 py-4 hover:bg-orange-500 transition duration-300">Orders : 0</NuxtLink></li>
          <li><NuxtLink to="/keranjang" class="block text-sm px-2 py-4 hover:bg-orange-500 transition duration-300">Cart</NuxtLink></li>
				</ul>
			</div>
		</nav>
    </header>
    <slot />
    <svg width="100%" height="100%" id="svg" viewBox="0 0 1440 390" xmlns="http://www.w3.org/2000/svg" class="mb-0 transition duration-300 ease-in-out delay-150"><defs><linearGradient id="gradient" x1="50%" y1="100%" x2="50%" y2="0%"><stop offset="5%" stop-color="#ff5c20"></stop><stop offset="95%" stop-color="#eb144c"></stop></linearGradient></defs><path d="M 0,400 C 0,400 0,200 0,200 C 104.87081339712918,240.39234449760767 209.74162679425837,280.78468899521533 297,274 C 384.25837320574163,267.21531100478467 453.9043062200957,213.25358851674642 550,178 C 646.0956937799043,142.74641148325358 768.6411483253588,126.20095693779905 861,139 C 953.3588516746412,151.79904306220095 1015.5311004784689,193.94258373205741 1107,209 C 1198.468899521531,224.05741626794259 1319.2344497607655,212.0287081339713 1440,200 C 1440,200 1440,400 1440,400 Z" stroke="none" stroke-width="0" fill="url(#gradient)" fill-opacity="1" class="transition-all duration-300 ease-in-out delay-150 path-0"></path></svg>
    <footer class="text-center bg-orange-500 lg:text-left">
      <div
        class="flex bg-orange-500 items-center justify-center p-6 lg:justify-between">
        <div class="mr-12 text-gray-50 hidden lg:block">
          <span>Get connected with us on social networks:</span>
        </div>
        <!-- Social network icons container -->
        <div class="flex justify-center">
          <a href="#!" class="mr-6 text-gray-50">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="currentColor"
              viewBox="0 0 24 24">
              <path
                d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z" />
            </svg>
          </a>
          <a href="#!" class="mr-6 text-gray-50">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="currentColor"
              viewBox="0 0 24 24">
              <path
                d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
            </svg>
          </a>
          <a href="#!" class="mr-6 text-gray-50">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 24 24">
              <path
                d="M7 11v2.4h3.97c-.16 1.029-1.2 3.02-3.97 3.02-2.39 0-4.34-1.979-4.34-4.42 0-2.44 1.95-4.42 4.34-4.42 1.36 0 2.27.58 2.79 1.08l1.9-1.83c-1.22-1.14-2.8-1.83-4.69-1.83-3.87 0-7 3.13-7 7s3.13 7 7 7c4.04 0 6.721-2.84 6.721-6.84 0-.46-.051-.81-.111-1.16h-6.61zm0 0 17 2h-3v3h-2v-3h-3v-2h3v-3h2v3h3v2z"
                fill-rule="evenodd"
                clip-rule="evenodd" />
            </svg>
          </a>
          <a href="#!" class="mr-6 text-gray-50">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="currentColor"
              viewBox="0 0 24 24">
              <path
                d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
            </svg>
          </a>
          <a href="#!" class="mr-6 text-gray-50">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="currentColor"
              viewBox="0 0 24 24">
              <path
                d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z" />
            </svg>
          </a>
          <a href="#!" class="text-gray-50">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="currentColor"
              viewBox="0 0 24 24">
              <path
                d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
            </svg>
          </a>
        </div>
      </div>

      <div class="mx-6 py-10 text-center md:text-left">
        <div class="grid-1 grid gap-8 md:grid-cols-2 lg:grid-cols-4">
          <div>
            <h6
              class="mb-4 flex text-gray-50 items-center justify-center font-semibold uppercase md:justify-start">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="mr-3 h-4 w-4">
                <path
                  d="M12.378 1.602a.75.75 0 00-.756 0L3 6.632l9 5.25 9-5.25-8.622-5.03zM21.75 7.93l-9 5.25v9l8.628-5.032a.75.75 0 00.372-.648V7.93zM11.25 22.18v-9l-9-5.25v8.57a.75.75 0 00.372.648l8.628 5.033z" />
              </svg>
              Websiteku.id
            </h6>
            <p class="text-gray-50">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, amet itaque consequuntur laborum maxime debitis maiores delectus repellendus architecto inventore!
            </p>
          </div>
          <div class="product">
            <h6
              class="mb-4 flex text-gray-50 justify-center font-semibold uppercase md:justify-start">
              Best Type Products
            </h6>
            <p class="mb-4 text-gray-50">Snack</p>
            <p class="mb-4 text-gray-50">Drink</p>
            <p class="mb-4 text-gray-50">Food</p>
            <p class="text-gray-50">Traditional Cake</p>
          </div>
          <div class="menu">
            <h6
              class="mb-4 flex justify-center text-gray-50 font-semibold uppercase md:justify-start">
              Menu
            </h6>
            <p class="mb-4 text-gray-50">Product</p>
            <p class="mb-4 text-gray-50">Cart</p>
            <p class="mb-4 text-gray-50">About Us</p>
            <p class="text-gray-50">Contact Us</p>
          </div>
          <div class="contact">
            <h6
              class="mb-4 flex text-gray-50 justify-center font-semibold uppercase md:justify-start">
              Contact Us
            </h6>
            <p class="mb-4 flex text-gray-50 items-center justify-center md:justify-start">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="mr-3 h-5 w-5">
                <path
                  d="M11.47 3.84a.75.75 0 011.06 0l8.69 8.69a.75.75 0 101.06-1.06l-8.689-8.69a2.25 2.25 0 00-3.182 0l-8.69 8.69a.75.75 0 001.061 1.06l8.69-8.69z" />
                <path
                  d="M12 5.432l8.159 8.159c.03.03.06.058.091.086v6.198c0 1.035-.84 1.875-1.875 1.875H15a.75.75 0 01-.75-.75v-4.5a.75.75 0 00-.75-.75h-3a.75.75 0 00-.75.75V21a.75.75 0 01-.75.75H5.625a1.875 1.875 0 01-1.875-1.875v-6.198a2.29 2.29 0 00.091-.086L12 5.43z" />
              </svg>
              Tigaraksa, TG 015, IND
            </p>
            <p class="mb-4 flex text-gray-50 items-center justify-center md:justify-start">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="mr-3 h-5 w-5">
                <path
                  d="M1.5 8.67v8.58a3 3 0 003 3h15a3 3 0 003-3V8.67l-8.928 5.493a3 3 0 01-3.144 0L1.5 8.67z" />
                <path
                  d="M22.5 6.908V6.75a3 3 0 00-3-3h-15a3 3 0 00-3 3v.158l9.714 5.978a1.5 1.5 0 001.572 0L22.5 6.908z" />
              </svg>
              websiteku.com
            </p>
            <p class="mb-4 flex text-gray-50 items-center justify-center md:justify-start">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="mr-3 h-5 w-5">
                <path
                  fill-rule="evenodd"
                  d="M1.5 4.5a3 3 0 013-3h1.372c.86 0 1.61.586 1.819 1.42l1.105 4.423a1.875 1.875 0 01-.694 1.955l-1.293.97c-.135.101-.164.249-.126.352a11.285 11.285 0 006.697 6.697c.103.038.25.009.352-.126l.97-1.293a1.875 1.875 0 011.955-.694l4.423 1.105c.834.209 1.42.959 1.42 1.82V19.5a3 3 0 01-3 3h-2.25C8.552 22.5 1.5 15.448 1.5 6.75V4.5z"
                  clip-rule="evenodd" />
              </svg>
              +62813880002133
            </p>
            <p class="flex text-gray-50 items-center justify-center md:justify-start">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="mr-3 h-5 w-5">
                <path
                  fill-rule="evenodd"
                  d="M7.875 1.5C6.839 1.5 6 2.34 6 3.375v2.99c-.426.053-.851.11-1.274.174-1.454.218-2.476 1.483-2.476 2.917v6.294a3 3 0 003 3h.27l-.155 1.705A1.875 1.875 0 007.232 22.5h9.536a1.875 1.875 0 001.867-2.045l-.155-1.705h.27a3 3 0 003-3V9.456c0-1.434-1.022-2.7-2.476-2.917A48.716 48.716 0 0018 6.366V3.375c0-1.036-.84-1.875-1.875-1.875h-8.25zM16.5 6.205v-2.83A.375.375 0 0016.125 3h-8.25a.375.375 0 00-.375.375v2.83a49.353 49.353 0 019 0zm-.217 8.265c.178.018.317.16.333.337l.526 5.784a.375.375 0 01-.374.409H7.232a.375.375 0 01-.374-.409l.526-5.784a.373.373 0 01.333-.337 41.741 41.741 0 018.566 0zm.967-3.97a.75.75 0 01.75-.75h.008a.75.75 0 01.75.75v.008a.75.75 0 01-.75.75H18a.75.75 0 01-.75-.75V10.5zM15 9.75a.75.75 0 00-.75.75v.008c0 .414.336.75.75.75h.008a.75.75 0 00.75-.75V10.5a.75.75 0 00-.75-.75H15z"
                  clip-rule="evenodd" />
              </svg>
              +02188927112335
            </p>
          </div>
        </div>
      </div>

      <!--Copyright section-->
      <div class="bg-orange-500 p-6 text-center">
        <span class="text-gray-50">Copyright ©2023</span>
        <a
          class="font-semibold text-gray-50"
          href="https://tailwind-elements.com/"
          >Websiteku Store. All right reserved</a
        >
      </div>
    </footer>
    </div>
</template>

<style scoped>
          .path-0{
            animation:pathAnim-0 4s;
            animation-timing-function: linear;
            animation-iteration-count: infinite;
          }
          @keyframes pathAnim-0{
            0%{
              d: path("M 0,400 C 0,400 0,200 0,200 C 104.87081339712918,240.39234449760767 209.74162679425837,280.78468899521533 297,274 C 384.25837320574163,267.21531100478467 453.9043062200957,213.25358851674642 550,178 C 646.0956937799043,142.74641148325358 768.6411483253588,126.20095693779905 861,139 C 953.3588516746412,151.79904306220095 1015.5311004784689,193.94258373205741 1107,209 C 1198.468899521531,224.05741626794259 1319.2344497607655,212.0287081339713 1440,200 C 1440,200 1440,400 1440,400 Z");
            }
            25%{
              d: path("M 0,400 C 0,400 0,200 0,200 C 83.29186602870817,206.1531100478469 166.58373205741634,212.3062200956938 263,208 C 359.41626794258366,203.6937799043062 468.956937799043,188.92822966507177 586,197 C 703.043062200957,205.07177033492823 827.5885167464116,235.98086124401914 913,226 C 998.4114832535884,216.01913875598086 1044.688995215311,165.14832535885168 1126,154 C 1207.311004784689,142.85167464114832 1323.6555023923445,171.42583732057415 1440,200 C 1440,200 1440,400 1440,400 Z");
            }
            50%{
              d: path("M 0,400 C 0,400 0,200 0,200 C 77.70334928229664,219.16746411483254 155.40669856459328,238.33492822966508 267,228 C 378.5933014354067,217.66507177033492 524.0765550239234,177.82775119617222 619,176 C 713.9234449760766,174.17224880382778 758.2870813397129,210.35406698564597 848,202 C 937.7129186602871,193.64593301435403 1072.775119617225,140.755980861244 1179,133 C 1285.224880382775,125.24401913875599 1362.6124401913876,162.622009569378 1440,200 C 1440,200 1440,400 1440,400 Z");
            }
            75%{
              d: path("M 0,400 C 0,400 0,200 0,200 C 117.65550239234452,196.23923444976077 235.31100478468903,192.47846889952152 320,216 C 404.68899521531097,239.52153110047848 456.41148325358836,290.32535885167465 537,266 C 617.5885167464116,241.67464114832535 727.043062200957,142.2200956937799 826,133 C 924.956937799043,123.7799043062201 1013.4162679425838,204.79425837320576 1114,231 C 1214.5837320574162,257.20574162679424 1327.2918660287082,228.60287081339712 1440,200 C 1440,200 1440,400 1440,400 Z");
            }
            100%{
              d: path("M 0,400 C 0,400 0,200 0,200 C 104.87081339712918,240.39234449760767 209.74162679425837,280.78468899521533 297,274 C 384.25837320574163,267.21531100478467 453.9043062200957,213.25358851674642 550,178 C 646.0956937799043,142.74641148325358 768.6411483253588,126.20095693779905 861,139 C 953.3588516746412,151.79904306220095 1015.5311004784689,193.94258373205741 1107,209 C 1198.468899521531,224.05741626794259 1319.2344497607655,212.0287081339713 1440,200 C 1440,200 1440,400 1440,400 Z");
            }
          }
</style>

<script setup>

if(typeof window !== "undefined"){
	const btn = document.querySelector("button.mobile-menu-button");
	const menu = document.querySelector(".mobile-menu");

	btn.addEventListener("click", () => {
		menu.classList.toggle("hidden");
	});
}
</script>