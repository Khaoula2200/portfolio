

<template>
	<div
		class="container mx-auto flex flex-col-reverse md:flex-col py-5 md:py-10 md:mt-10"
	>
	<p
		class="pb-10 font-general-semibold text-3xl sm:text-4xl font-semibold text-primary-dark dark:text-primary-light "
	>
		Contact me
	</p>
		<div class="socialsAndDetails">
		<div
				class="flex flex-col justify-center items-center  sm:mb-10 socialsOrDetails"
			>
				<ul class=" socialLinksBox flex gap-2 sm:gap-4">
					<a
						v-for="social in socials"
						:key="social.id"
						:href="social.url"
						target="__blank"
						class="text-gray-400 hover:text-sky-700 dark:hover:text-sky-700 cursor-pointer rounded-lg  shadow-sm p-4 duration-500"
					>
						<font-awesome-icon class="w-5 sm:w-8 h-5 sm:h-8" :icon="[social.type,social.icon]" />
					</a>
				</ul>
			</div>

		<ContactDetails class=" socialsOrDetails" :contacts="contacts" />
	</div>
	</div>
</template>

<script>
import feather from 'feather-icons';
import ContactDetails from '@/components/contact/ContactDetails.vue';
import {socialLinks} from '../../data/socialLinks';

export default {
	components: {
		ContactDetails,
	},
	data: () => {
		return {
			socials:socialLinks,
			contacts: [
				{
					id: 1,
					name: 'Rabat, MOROCCO',
					icon: 'map-pin',
				},
				{
					id: 2,
					name: 'younouskhaoula22@gmail.com',
					icon: 'mail',
				},
				{
					id: 3,
					name: '+212641620786', 
					icon: 'phone',
				},
			],
		};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>
<style>
.socialLinksBox{
	flex-direction: column !important;
}
.socialsAndDetails{
	display: flex;
	flex-direction: row-reverse !important;
	justify-content: center;
}
.socialsOrDetails{
	width: calc(50%);
}
</style>
