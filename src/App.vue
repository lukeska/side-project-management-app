<script setup>
import CardsCompact from "./components/CardsCompact.vue";
import CardsDetailed from "./components/CardsDetailed.vue";

import { ref } from "vue";
import {
	IconSortDescending,
	IconAntennaBars5,
	IconWifi,
	IconBattery,
	IconMoonFilled,
	IconSunFilled,
} from "@tabler/icons-vue";

let compact = ref(true);
let dark = ref(true);
</script>

<template>
	<div :class="[dark ? 'dark' : '']">
		<div
			class="w-full h-full p-20 bg-zinc-100 dark:bg-[#535353] transition duration-300 ease-out"
		>
			<div class="w-[387px] mx-auto mb-6">
				<button
					@click="dark = !dark"
					class="w-10 h-10 rounded-full bg-[#f6f6f6] dark:bg-[#282828] flex items-center justify-center shadow-md"
				>
					<IconMoonFilled class="text-white" v-if="dark" />
					<IconSunFilled class="text-black" v-if="!dark" />
				</button>
			</div>

			<div
				class="p-1.5 bg-white dark:bg-[#222222] w-[387px] h-[824px] mx-auto rounded-[40px] shadow-lg"
			>
				<div
					class="relative w-[375px] h-[812px] bg-[#f6f6f6] dark:bg-[#282828] dark:text-white mx-auto rounded-[34px] py-10 overflow-hidden"
				>
					<!-- <div
						class="absolute w-[1080px] opacity-0 top-[-83px] left-[-118px]"
					>
						<img src="design_light_mode.jpg" alt="" />
					</div> -->
					<div
						class="absolute left-0 flex items-center justify-between w-full px-8 top-8"
					>
						<div>09:41</div>
						<div class="flex items-center justify-end space-x-1">
							<IconAntennaBars5 />
							<IconWifi />
							<IconBattery />
						</div>
					</div>
					<div class="pt-8 px-7">
						<h1 class="text-xl tracking-wide">Active Projects</h1>
					</div>
					<div class="flex items-center justify-between my-5 px-7">
						<div
							class="relative text-sm bg-[#efefef] dark:bg-[#333333] ring-2 ring-[#efefef] dark:ring-[#333333] rounded-full w-56"
						>
							<span
								:class="[
									compact
										? 'translate-x-0'
										: 'translate-x-full',
									'absolute top-0 left-0 inline-block bg-white dark:bg-[#202020] rounded-full w-28 h-9 transition duration-300 ease-out',
								]"
							></span>
							<button
								:class="[
									compact
										? 'text-black dark:text-white'
										: 'text-zinc-500 dark:text-[#878787]',
									'relative text-center w-28 h-9 transition',
								]"
								class=""
								@click="compact = true"
							>
								Compact
							</button>
							<button
								:class="[
									!compact
										? 'text-black dark:text-white'
										: 'text-zinc-500 dark:text-[#878787]',
									'relative text-center w-28 h-9 transition',
								]"
								@click="compact = false"
							>
								Detailed
							</button>
						</div>
						<div>
							<button
								class="bg-white dark:bg-[#202020] ring-2 ring-[#efefef] dark:ring-[#202020] rounded-full h-9 w-14 text-center"
							>
								<IconSortDescending
									:size="16"
									class="mx-auto"
								/>
							</button>
						</div>
					</div>
					<div class="overflow-hidden">
						<div
							:class="[
								compact ? 'translate-x-0' : '-translate-x-full',
								'flex transition duration-300 ease-out',
							]"
						>
							<CardsCompact class="w-full shrink-0" />
							<CardsDetailed class="w-full shrink-0" />
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
