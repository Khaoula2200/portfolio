
<template>
	<div class="container mx-auto">
		<div
			class="pt-20 sm:pt-30 pb-10 mt-20 border-b-2 border-primary-light dark:border-secondary-dark"
		>
			<!-- Footer social links -->
			<div
				class=" flex flex-col justify-center items-center mb-12 sm:mb-20"
			>
				<p
					class="pt-5 pb-5 font-general-semibold text-3xl sm:text-4xl font-semibold text-primary-dark dark:text-primary-light mb-5"
				>
					Skills
				</p>
				<ul class="skills-container flex gap-10 sm:gap-10">
					<div
						v-for="skill in skills"
						:key="skill.name"
						target="__blank"
						:id="'skill-'+skill.id"
						class="skillBox text-gray-400 hover:text-sky-700 dark:hover:text-sky-700 cursor-pointer rounded-lg bg-gray-50 dark:bg-ternary-dark hover:bg-gray-100 shadow-sm p-4 duration-500"
					>
						<font-awesome-icon class="myIcon" :icon="[skill.type,skill.icon]" />
						<span>{{ skill.name }}</span>

					</div>
				</ul>
			</div>

			<!-- Footer copyright -->
		</div>
	</div>
</template>
<script>
import { mySkills } from '../../data/mySkills';

export default {
	components: {  },
	data() {
		return {
			iconStyle:"fa-brands",
			skills:mySkills
		};
	},
	mounted() {
	},
	updated() {
	},
};
</script>


<style scoped>

.myIcon{
	font-size: 100px;
}
.skills-container{
	flex-wrap: wrap !important;
	justify-content: center;
}
.skillBox{
	display: flex;
	flex-direction: column;
	justify-content: center;
	padding: 20px 0;
	min-width: 165px !important;
	transform: translatey(0px);
	transform: translatex(0px);
}
#skill-1,#skill-3{
	animation: float 4s ease-in-out infinite;
	
}
#skill-5,#skill-7{
animation: float2 4s ease-in-out infinite;
}
#skill-9,#skill-2{
animation: float3 4s ease-in-out infinite;
}
#skill-4,#skill-8{
animation: float4 4s ease-in-out infinite;
}
#skill-6{
animation: float5 4s ease-in-out infinite;
}
@keyframes float {
	0% {
		transform: translatex(0px);
	}
	50% {
		transform: translatex(8px);
	}
	100% {
		transform: translatex(0px);
	}
}
@keyframes float2 {
	0% {
		transform: translatey(0px);
	}
	50% {
		transform: translatey(-8px);
	}
	100% {
		transform: translatey(0px);
	}
}
@keyframes float3 {
	0% {
		transform: translatex(0px);
	}
	50% {
		transform: translatex(-8px);
	}
	100% {
		transform: translatex(0px);
	}
}
@keyframes float4 {
	0% {
		transform: translate(0px,0px);
	}
	50% {
		transform: translate(8px,8px);
	}
	100% {
		transform: translate(0px,0px);
	}
}
@keyframes float5 {
	0% {
		transform: translate(-0px,-0px);
	}
	50% {
		transform: translate(-8px,-8px);
	}
	100% {
		transform: translate(-0px,-0px);
	}
}
</style>
