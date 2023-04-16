
<template>
	<div class="container mx-auto">
		<div
			class="pt-20 sm:pt-30 pb-8 mt-20"
		>
			<FooterCopyright />
		</div>
	</div>
</template>

<script>
import feather from 'feather-icons';
import FooterCopyright from './FooterCopyright.vue';
import { socialLinks } from '../../data/socialLinks';

export default {
	components: { FooterCopyright },
	data() {
		return {
			socials: socialLinks,
		};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>


<style scoped></style>
