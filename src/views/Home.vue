
<template>
	<div class="container mx-auto">
		<AppBanner class="mb-5 sm:mb-8" />

		<AboutMe />
		<SkillsGrid />
		<ProjectsGrid />
		<ContactMe />

	
	</div>
</template>

<script>
import AppBanner from '@/components/shared/AppBanner';
import ProjectsGrid from '../components/projects/ProjectsGrid.vue';
import SkillsGrid from '../components/skills/SkillsGrid.vue';
import AboutMe from '@/components/about/AboutMe';
import ContactMe from '../components/contact/ContactMe.vue';

export default {
	name: 'Home',
	components: {
		AppBanner,
		ProjectsGrid,
		SkillsGrid,
		AboutMe,
		ContactMe,
	},
};
</script>


<style scoped></style>
