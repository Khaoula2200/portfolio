
<template>
	<div class="flex justify-center items-center text-center">
		<div
			class="font-general-regular text-lg text-ternary-dark dark:text-ternary-light"
		>
			&copy; {{ copyrightDate }}.
			<span>
				{{ projectName }}
			</span>
		</div>
	</div>
</template>

<script>

export default {
	components: {
	},
	data: () => {
		return {
			copyrightDate: new Date().getFullYear(),
			projectName: 'Khaoula YOUNOUS',
			author: 'Khaoula YOUNOUS',
		};
	},
};
</script>

<style lang="scss" scoped></style>
