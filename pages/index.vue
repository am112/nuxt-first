<template>
	<Carousel
		class="m-8 max-h-72"
		:opts="{
			align: 'start',
			loop: true,
		}"
		:plugins="[
			Autoplay({
				delay: 5000,
			}),
		]"
	>
		<CarouselContent>
			<CarouselItem v-for="(_, index) in 5" :key="index">
				<div class="p-5">
					<Card>
						<CardContent class="flex items-center justify-center p-20">
							<span class="text-4xl font-semibold">{{ index + 1 }}</span>
						</CardContent>
					</Card>
				</div>
			</CarouselItem>
		</CarouselContent>
		<CarouselPrevious />
		<CarouselNext />
	</Carousel>
</template>
<script setup>
import Autoplay from "embla-carousel-autoplay";
</script>
