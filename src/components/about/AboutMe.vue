
<template>
	<div class=" flex flex-row justify-center sm:flex sm:gap-10 mt-10 sm:mt-20">
		
		<div class="about-text-wrapper p-20 rounded-xl w-full sm:w-2/4 text-justify">
			<div>
			
				<p
					v-for="contentElement in content"
					:key="contentElement.text"
					class="font-general-regular mb-4 text-ternary-dark dark:text-ternary-light text-lg"
				>
					{{ contentElement.text }}
				</p>
		</div>
			<ul>
				<li
					v-for="inf in info"
					:key="inf.id"
					class="font-general-regular mb-4 text-ternary-dark dark:text-ternary-light text-lg"
				>
					
					<span>
						{{ inf.element }}: 
					</span>
					<span>
						{{ inf.answer }}
					</span>
			</li>
			</ul>
		</div>
	</div>
</template>
<script>
import { AboutMe } from '../../data/AboutMe'
import { info } from '../../data/info'
export default {
	setup() {
		return {
			content:AboutMe,
			info:info
		};
	},
};
</script>
<style scoped>
.about-text-wrapper{
	background-color:rgba(0,0,0,0.2);
	backdrop-filter: blur(3px); 

}
</style>