<script>
export default {
	props: ['contacts'],
};
</script>

<template>
	<div class="flex flex-col justify-center  w-full md:w-1/2">
		<div class="text-left max-w-xl px-6">
			<ul class="flex flex-col justify-center font-general-regular ">
				<li class="flex flex-row" v-for="contact in contacts" :key="contact.id">
					<i
						:data-feather="contact.icon"
						class="w-5 text-gray-500 dark:text-gray-400 mr-4"
					></i>
					<a
						href="#"
						class="text-lg mb-4 text-ternary-dark dark:text-ternary-light"
						:class="
							contact.icon === 'mail' || contact.icon === 'phone'
								? 'hover:underline cursor-pointer'
								: ''
						"
						aria-label="Website and Phone"
					>
						{{ contact.name }}
					</a>
				</li>
			</ul>
		</div>
	</div>
</template>

<style lang="scss" scoped></style>
