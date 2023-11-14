<script setup>
import { squircleObserver } from "corner-smoothing";
import { onMounted } from "vue";
import {
	IconMailBolt,
	IconFlame,
	IconCalendar,
	IconClockRecord,
} from "@tabler/icons-vue";

onMounted(() => {
	let squircles = document.getElementsByClassName("squircle");
	for (let i = 0; i < squircles.length; i++) {
		squircleObserver(squircles[i], {
			cornerRadius: 36,
			borderWidth: 1,
		});
	}
});
</script>

<template>
	<div class="px-4 space-y-3">
		<!-- Newsletter -->
		<div class="px-6 py-4 text-white bg-zinc-900 squircle">
			<div class="flex items-center justify-between">
				<div class="flex items-center font-semibold">
					<div
						class="inline-flex items-center justify-center w-8 h-8 mr-3 rounded-lg bg-neutral-700"
					>
						<IconMailBolt :size="18" />
					</div>
					Newsletter
				</div>
				<div class="flex items-center text-sm">
					<div class="inline-flex items-center justify-center mr-1">
						<IconFlame :size="16" />
					</div>
					needs attention
				</div>
			</div>
			<div
				class="w-full h-1.5 mt-2 overflow-hidden rounded-full bg-neutral-700"
			>
				<div
					class="h-1.5 bg-orange-500 rounded-full ring-2 ring-zinc-900"
					style="width: 62%"
				></div>
			</div>
			<div class="flex items-center justify-between mt-4 text-zinc-100">
				<div class="space-y-2 text-xs">
					<div class="flex items-center space-x-2">
						<IconCalendar :size="14" color="#f97316" />
						<span class="text-neutral-400">Next meet: </span>
						<span>November 14th</span>
					</div>
					<div class="flex items-center space-x-2">
						<IconClockRecord :size="14" color="#f97316" />
						<span class="text-neutral-400">Best move: </span>
						<span>Write 2 posts</span>
					</div>
				</div>
				<div class="text-4xl font-semibold">62%</div>
			</div>
		</div>
		<!-- Wirekit -->
		<div class="px-6 py-4 text-stone-800 bg-lime-300 squircle">
			<div class="flex items-center justify-between">
				<div class="flex items-center font-semibold">
					<div
						class="inline-flex items-center justify-center w-8 h-8 mr-3 rounded-lg bg-[#b8e15d]"
					>
						<IconMailBolt :size="18" class="text-white" />
					</div>
					Wirekit
				</div>
				<div class="flex items-center text-sm">active last 10 days</div>
			</div>
			<div
				class="w-full h-1.5 mt-2 overflow-hidden rounded-full bg-[#b8e15d]"
			>
				<div
					class="h-1.5 bg-lime-600 rounded-full ring-2 ring-lime-300"
					style="width: 78%"
				></div>
			</div>
			<div class="flex items-center justify-between mt-4">
				<div class="space-y-2 text-xs">
					<div class="flex items-center space-x-2">
						<IconCalendar :size="14" class="text-lime-600" />
						<span class="text-lime-600">Next meet: </span>
						<span>November 14th</span>
					</div>
					<div class="flex items-center space-x-2">
						<IconClockRecord :size="14" class="text-lime-600" />
						<span class="text-lime-600">Best move: </span>
						<span>Update waitlist</span>
					</div>
				</div>
				<div class="text-4xl font-semibold">78%</div>
			</div>
		</div>
		<!-- Dashkit -->
		<div class="px-6 py-4 bg-indigo-100 text-stone-800 squircle">
			<div class="flex items-center justify-between">
				<div class="flex items-center font-semibold">
					<div
						class="inline-flex items-center justify-center w-8 h-8 mr-3 bg-indigo-200 rounded-lg"
					>
						<IconMailBolt :size="18" class="text-white" />
					</div>
					Dashkit
				</div>
				<div class="flex items-center text-sm">active last 4 days</div>
			</div>
			<div
				class="w-full h-1.5 mt-2 overflow-hidden rounded-full bg-indigo-200"
			>
				<div
					class="h-1.5 bg-indigo-500 rounded-full ring-2 ring-lime-300"
					style="width: 45%"
				></div>
			</div>
			<div class="flex items-center justify-between mt-4">
				<div class="space-y-2 text-xs">
					<div class="flex items-center space-x-2">
						<IconCalendar :size="14" class="text-indigo-500" />
						<span class="text-stone-400">Next meet: </span>
						<span>November 14th</span>
					</div>
					<div class="flex items-center space-x-2">
						<IconClockRecord :size="14" class="text-indigo-500" />
						<span class="text-stone-400">Best move: </span>
						<span>Update waitlist</span>
					</div>
				</div>
				<div class="text-4xl font-semibold">45%</div>
			</div>
		</div>
	</div>
</template>
