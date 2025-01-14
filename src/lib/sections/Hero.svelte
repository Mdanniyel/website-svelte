<script>
	import WaMessage from "./WaMessage.svelte";
	import recommendations from "$lib/recommendations.json";
</script>

<section>
	<div class="relative -mt-16 h-screen rounded-t-3xl bg-white">
		<div class="relative flex h-full flex-col justify-between space-x-1.5 md:flex-row-reverse">
			<!-- text and bottens -->
			<div class="mx-2.5 mt-3 self-center">
				<div class="mt-7 text-center">
					<h1
						class="mb-5 bg-gradient-to-r from-stone-900 to-stone-700 bg-clip-text text-3xl font-bold tracking-wider text-transparent"
					>
						מורה אישי להצלחה
					</h1>
					<p class="text-center text-lg font-light tracking-wide">
						אחרי מאות תלמידים ועשור של ניסיון, אני יכול להגיד בבטחון שאני יודע ללמד כל תלמיד איך
						להצליח במבחנים ובכיתה. כל תלמיד יכול להצליח
					</p>
				</div>
				<div class="mt-4 flex justify-center gap-3.5 text-center text-3xl">
					<button
						type="button"
						aria-label="Phone Number"
						class="flex justify-center w-1/2 fill-white grow rounded-lg border border-black bg-gradient-to-r from-stone-900 to-stone-800 py-1.5 text-white hover:bg-gradient-to-br focus:ring-4 focus:ring-blue-300 dark:focus:ring-blue-800"
					>
						<svg class="h-12" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="122.88px" height="122.267px" viewBox="0 0 122.88 122.267" enable-background="new 0 0 122.88 122.267" xml:space="preserve"><g><path d="M33.822,50.291c4.137,7.442,8.898,14.604,15.074,21.133C55.1,77.984,62.782,83.962,72.771,89.03l0.01,0.005l0.002-0.005 c0.728,0.371,1.421,0.362,2.072,0.118c0.944-0.353,1.927-1.137,2.883-2.086c0.729-0.726,1.643-1.924,2.631-3.223 c3.846-5.054,8.601-11.301,15.314-8.193c0.142,0.065,0.276,0.141,0.402,0.226l22.373,12.852c0.08,0.046,0.157,0.095,0.23,0.147 c2.966,2.036,4.177,5.172,4.19,8.683c0.014,3.621-1.329,7.674-3.274,11.101c-2.565,4.517-6.387,7.502-10.761,9.525 c-4.17,1.928-8.798,2.954-13.267,3.608c-6.989,1.025-13.578,0.374-20.288-1.692c-6.55-2.017-13.176-5.385-20.4-9.86l-0.526-0.326 c-3.326-2.06-6.906-4.276-10.389-6.904C31.108,93.296,18.007,79.283,9.512,63.904C2.361,50.958-1.552,36.995,0.581,23.681 C1.75,16.375,4.901,9.743,10.333,5.35c4.762-3.853,11.188-5.94,19.448-5.203c0.973,0.084,1.793,0.639,2.255,1.419l0.006-0.003 l14.324,24.27c2.11,2.718,2.344,5.415,1.203,8.096c-0.943,2.218-2.892,4.251-5.476,6.168c-0.786,0.65-1.708,1.325-2.659,2.021 C36.236,44.459,32.578,47.136,33.822,50.291L33.822,50.291z M44.67,75.422C38.066,68.44,33.035,60.88,28.695,53.065 c-0.076-0.123-0.144-0.253-0.202-0.39c-3.174-7.459,2.52-11.625,7.493-15.262c0.845-0.618,1.663-1.217,2.401-1.829l0.002,0.003 c0.043-0.036,0.088-0.071,0.135-0.105c1.843-1.354,3.171-2.647,3.678-3.837c0.289-0.679,0.182-1.426-0.466-2.265 c-0.111-0.129-0.213-0.271-0.303-0.423L27.795,5.852c-5.869-0.241-10.419,1.321-13.784,4.044 c-4.239,3.429-6.723,8.759-7.674,14.699c-1.905,11.894,1.716,24.594,8.292,36.5c8.078,14.623,20.575,27.977,32.864,37.25 c3.379,2.55,6.776,4.653,9.932,6.607l0.526,0.326c6.818,4.223,13.017,7.386,19.052,9.244c5.876,1.809,11.634,2.38,17.729,1.486 c4.009-0.587,8.113-1.485,11.668-3.129c3.351-1.55,6.248-3.785,8.134-7.104c1.496-2.637,2.53-5.653,2.521-8.222 c-0.006-1.63-0.472-3.029-1.605-3.844L93.2,80.93c-2.461-1.081-5.629,3.081-8.193,6.45c-1.104,1.452-2.125,2.792-3.156,3.817 c-1.477,1.466-3.118,2.723-4.962,3.411c-2.136,0.799-4.395,0.834-6.755-0.37l0.002-0.004C59.522,88.849,51.323,82.457,44.67,75.422 L44.67,75.422z"/></g></svg>
					</button>
					<button
						type="button"
						aria-label="Whatsapp Number"
						class="flex justify-center w-1/2 grow rounded-lg border border-black py-1.5 hover:bg-gradient-to-br focus:ring-4 focus:ring-green-300 dark:focus:ring-green-800"
					>
						<svg class="h-12" xmlns="http://www.w3.org/2000/svg" shape-rendering="geometricPrecision" text-rendering="geometricPrecision" image-rendering="optimizeQuality" fill-rule="evenodd" clip-rule="evenodd" viewBox="0 0 510 512.459"><path fill="#111B21" d="M435.689 74.468C387.754 26.471 324 .025 256.071 0 116.098 0 2.18 113.906 2.131 253.916c-.024 44.758 11.677 88.445 33.898 126.946L0 512.459l134.617-35.311c37.087 20.238 78.85 30.891 121.345 30.903h.109c139.949 0 253.88-113.917 253.928-253.928.024-67.855-26.361-131.645-74.31-179.643v-.012zm-179.618 390.7h-.085c-37.868-.011-75.016-10.192-107.428-29.417l-7.707-4.577-79.886 20.953 21.32-77.889-5.017-7.987c-21.125-33.605-32.29-72.447-32.266-112.322.049-116.366 94.729-211.046 211.155-211.046 56.373.025 109.364 22.003 149.214 61.903 39.853 39.888 61.781 92.927 61.757 149.313-.05 116.377-94.728 211.058-211.057 211.058v.011zm115.768-158.067c-6.344-3.178-37.537-18.52-43.358-20.639-5.82-2.119-10.044-3.177-14.27 3.178-4.225 6.357-16.388 20.651-20.09 24.875-3.702 4.238-7.403 4.762-13.747 1.583-6.343-3.178-26.787-9.874-51.029-31.487-18.86-16.827-31.597-37.598-35.297-43.955-3.702-6.355-.39-9.789 2.775-12.943 2.849-2.848 6.344-7.414 9.522-11.116s4.225-6.355 6.343-10.581c2.12-4.238 1.06-7.937-.522-11.117-1.584-3.177-14.271-34.409-19.568-47.108-5.151-12.37-10.385-10.69-14.269-10.897-3.703-.183-7.927-.219-12.164-.219s-11.105 1.582-16.925 7.939c-5.82 6.354-22.209 21.709-22.209 52.927 0 31.22 22.733 61.405 25.911 65.642 3.177 4.237 44.745 68.318 108.389 95.812 15.135 6.538 26.957 10.446 36.175 13.368 15.196 4.834 29.027 4.153 39.96 2.52 12.19-1.825 37.54-15.353 42.824-30.172 5.283-14.818 5.283-27.529 3.701-30.172-1.582-2.641-5.819-4.237-12.163-7.414l.011-.024z"/></svg>
					</button>
				</div>
			</div>
			<div class="relative my-4 flex overflow-hidden">
				
				<div class="grow overflow-hidden px-3 min-w-64">
					<div class="slide-top">
						{#each recommendations.slice(0) as recommendation}
							<WaMessage text={recommendation}/>
						{/each}
						{#each recommendations.slice(0) as recommendation}
							<WaMessage text={recommendation}/>
						{/each}
					</div>
				</div>
				
				<div class="hidden grow overflow-hidden px-3 min-w-64 lg:block">
					<div class="slide-top">
						{#each recommendations.slice(4) as recommendation}
							<WaMessage text={recommendation}/>
						{/each}
					</div>
				</div>
				
				<div class="hidden grow overflow-hidden px-3 min-w-64 xl:block">
					<div class="slide-top">
						{#each recommendations.slice(2) as recommendation}
							<WaMessage text={recommendation}/>
						{/each}
					</div>
				</div>

				<div
					class="pointer-events-none absolute inset-x-0 top-0 h-32 bg-gradient-to-b from-white"
				></div>
				<div
					class="pointer-events-none absolute inset-x-0 bottom-0 h-32 bg-gradient-to-t from-white"
				></div>
			</div>
		</div>
	</div>
</section>

<style>
	.slide-top {
		animation: slide-top 70s linear infinite both;
	}

	@keyframes slide-top {
		100% {
			transform: translateY(-50%);
		}
	}
</style>
