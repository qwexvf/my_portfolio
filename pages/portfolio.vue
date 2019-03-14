<template>
	<div>
		<div class="uk-child-width-1-3@m uk-grid-match" uk-grid>
			<div class="uk-width-1-1 uk-row-first">
				<h1 class="uk-heading-large">
					Portfolio
				</h1>
				<p class="uk-heading-medium">
					Projects
				</p>
			</div>
		</div>
		<vk-grid
		gutter="medium"
		class="uk-child-width-expands@s uk-text-conter uk-child-width-1-2@m"
		>
		<div class="uk-card uk-card-default uk-card-body uk-width-1-2@m">
			<h3 class="uk-card-title">Default</h3>
			<p>Lorem ipsum <a href="#">dolor</a> sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
		</div>
		</vk-grid>
		<vk-grid
		gutter="medium"
		class="uk-child-width-expands@s uk-text-conter uk-child-width-1-2@m"
		>
		<div class="uk-card uk-card-default uk-card-body uk-width-1-2@m">
			<h3 class="uk-card-title">Default</h3>
			<p>Lorem ipsum <a href="#">dolor</a> sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
		</div>
		</vk-grid>
	</div>
</template>

<script lang="ts">
import {
	Component,
	Vue
} from "nuxt-property-decorator"

@Component({
	components: {
	}
})
export default class extends Vue {
}
</script>
