<template>
	<section
		class=" flex flex-col sm:justify-between items-center sm:flex-row pt-40 pb-40"
	>
		<div class="w-full md:w-2/4 text-left">
			
			<h1
				class="font-general-semibold text-3xl md:text-3xl xl:text-4xl text-center sm:text-center text-ternary-dark dark:text-primary-light uppercase"
			>
				Hi, I'm Khaoula
			</h1>
			<hr class="w-48 h-1 mx-auto my-4 bg-gray-300 border-0 rounded md:my-10 dark:bg-gray-500">

			<p
				class="font-general-medium mt-2 text-lg sm:text-xl  xl:text-2xl text-center sm:text-center leading-none text-gray-400"
			>
				I'm a web Developer 
			</p>
			<div class="flex flex-row pt-12 justify-center sm:flex ">
				
			
				<router-link
			to="/projects"
			class=" font-general-medium block text-left text-lg font-medium text-primary-dark dark:text-ternary-light hover:text-sky-700 dark:hover:text-sky-300  sm:mx-4 mb-2 sm:py-2 border-t-2 pt-3 sm:pt-2 sm:border-t-0 border-primary-light dark:border-secondary-dark"
			aria-label="See Projects"
			>
					<Button
						title="See Projects"
						class="text-md font-general-medium bg-sky-700 hover:bg-sky-700 text-white shadow-sm rounded-md px-5 py-2.5 duration-300"
					
						aria-label="projects btn"
					/>
					</router-link>
			</div>
		</div>

		<!-- Banner right illustration -->
		<div class="w-full md:w-2/4 text-right float-right">
			<img
			class="astronaut"
				src="@/assets/images/astronaut.png"
				alt="Astronaut"
			/>
		</div>
	</section>
</template>

<script>
import feather from 'feather-icons';
import Button from '../reusable/Button.vue';

export default {
	name: 'Home',
	components: {
		Button,
	},
	data: () => {
		return {
			theme: '',
		};
	},
	created() {
		this.theme = localStorage.getItem('theme') || 'light';
	},
	mounted() {
		feather.replace();
		this.theme = localStorage.getItem('theme') || 'light';
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>


<style scoped>



@keyframes float {
	0% {
		transform: translatey(0px);
	}
	50% {
		transform: translatey(-20px);
	}
	100% {
		transform: translatey(0px);
	}
}

.astronaut{
	transform: translatey(0px);
	animation: float 6s ease-in-out infinite;
}

</style>
