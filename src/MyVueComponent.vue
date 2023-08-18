<template>
	<div :style="styles">{{ text }}</div>
</template>

<script lang="ts">
import { CreatePack, MojitoComponentProps } from "@drinkjs/mojito-vue-pack";
import { defineComponent } from "vue";

const Text = defineComponent({
	props: {
		...MojitoComponentProps,
		text: String,
	},
});

export default Text;

export const PackText = CreatePack(Text, {
	name: "文本",
	category: "基础组件",
	props: {
		text: {
			name: "文字",
			type: "string",
			default: "这里显示文本...",
		},
	},
});
</script>
