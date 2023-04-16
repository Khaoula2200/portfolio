<script>
export default {
	props: ['showModal', 'isOpen'],
};
</script>

<template>
	<div
		:class="isOpen ? 'block' : 'hidden'"
		class="m-0 sm:ml-4 mt-5 sm:mt-3 sm:flex p-5 sm:p-0 justify-center items-center shadow-lg sm:shadow-none"
	>
		<router-link
			to="/skills"
			class="font-general-medium block text-left text-lg font-medium text-primary-dark dark:text-ternary-light hover:text-sky-700 dark:hover:text-sky-300  sm:mx-4 mb-2 sm:py-2 "
			aria-label="Skills"
			>Skills</router-link
		>
		<router-link
			to="/projects"
			class="font-general-medium block text-left text-lg font-medium text-primary-dark dark:text-ternary-light hover:text-sky-700 dark:hover:text-sky-300  sm:mx-4 mb-2 sm:py-2 "
			aria-label="Projects"
			>Projects</router-link
		>
		
		<router-link
			to="/about"
			class="font-general-medium block text-left text-lg font-medium text-primary-dark dark:text-ternary-light hover:text-sky-700 dark:hover:text-sky-300  sm:mx-4 mb-2 sm:py-2 border-t-2 pt-3 sm:pt-2 sm:border-t-0 border-primary-light dark:border-secondary-dark"
			aria-label="About Me"
			>About Me</router-link
		>
		<div
			class="border-t-2 pt-3 sm:pt-0 sm:border-t-0 border-primary-light dark:border-secondary-dark"
		>
		
		<a
					download="YOUNOUS-khaoula.pdf"
					href="/files/YOUNOUS-khaoula.pdf"
					class="sm:hidden flex justify-center items-center w-36 sm:w-48  mb-6 sm:mb-0 text-lg border border-sky-200 dark:border-ternary-dark py-2.5 sm:py-3 shadow-lg rounded-lg bg-sky-50 focus:ring-1 focus:ring-sky-900 hover:bg-sky-700 text-gray-500 hover:text-white duration-500 "
					aria-label="Download Resume"
				>
					<i
						data-feather="arrow-down-circle"
						class="ml-0 sm:ml-1 mr-2 sm:mr-3 w-5 sm:w-6 duration-100"
					></i>
					<span
						class="text-sm sm:text-lg font-general-medium duration-100"
						>Download CV</span
					></a
				>
		</div>
	</div>
</template>

<style lang="scss" scoped></style>
