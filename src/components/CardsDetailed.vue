<script setup>
import { onMounted } from "vue";
import {
	IconMailBolt,
	IconFlame,
	IconCalendar,
	IconClockRecord,
} from "@tabler/icons-vue";
</script>

<template>
	<div class="">
		<!-- Newsletter -->
		<div class="pt-4 pb-2 px-7 text-zinc-900 dark:text-white">
			<div class="flex items-center justify-between">
				<div class="flex items-center font-semibold">
					<div
						class="inline-flex items-center justify-center w-8 h-8 mr-3 text-white rounded-lg bg-zinc-900"
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
				class="w-full h-1.5 mt-2 overflow-hidden rounded-full bg-neutral-300 dark:bg-[#393939]"
			>
				<div
					class="h-1.5 bg-orange-500 rounded-full ring-2 ring-[#f6f6f6] dark:ring-[#282828]"
					style="width: 62%"
				></div>
			</div>
			<div
				class="flex items-center justify-between mt-4 text-zinc-900 dark:text-white"
			>
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
			<!-- Tags -->
			<div
				class="py-4 mt-4 space-y-2 overflow-x-auto text-xs border-t text-neutral-400 border-neutral-200 dark:border-zinc-900"
			>
				<div class="flex space-x-2">
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#383838] whitespace-nowrap"
						>Explore other mailing services</span
					>
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#383838] whitespace-nowrap"
						>Explore other mailing services</span
					>
				</div>
				<div class="flex space-x-2">
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#383838] whitespace-nowrap"
						>Follow up: Edition #47</span
					>
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#383838] whitespace-nowrap"
						>Review: Group idea for collaboration</span
					>
				</div>
			</div>
		</div>
		<!-- Wirekit -->
		<div
			class="pt-4 pb-2 bg-white dark:bg-[#343434] px-7 text-zinc-900 dark:text-white"
		>
			<div class="flex items-center justify-between">
				<div class="flex items-center font-semibold">
					<div
						class="inline-flex items-center justify-center w-8 h-8 mr-3 rounded-lg bg-lime-300"
					>
						<IconMailBolt :size="18" class="text-white" />
					</div>
					Wirekit
				</div>
				<div class="flex items-center text-sm">active last 10 days</div>
			</div>
			<div
				class="w-full h-1.5 mt-2 overflow-hidden rounded-full bg-neutral-300 dark:bg-[#3f3f3f]"
			>
				<div
					class="h-1.5 bg-lime-300 rounded-full ring-2 ring-white dark:ring-[#343434]"
					style="width: 78%"
				></div>
			</div>
			<div class="flex items-center justify-between mt-4">
				<div class="space-y-2 text-xs">
					<div class="flex items-center space-x-2">
						<IconCalendar :size="14" class="text-lime-300" />
						<span class="text-neutral-400">Next meet: </span>
						<span>November 14th</span>
					</div>
					<div class="flex items-center space-x-2">
						<IconClockRecord :size="14" class="text-lime-300" />
						<span class="text-neutral-400">Best move: </span>
						<span>Update waitlist</span>
					</div>
				</div>
				<div class="text-4xl font-semibold">78%</div>
			</div>
			<!-- Tags -->
			<div
				class="py-4 mt-4 space-y-2 overflow-x-auto text-xs border-t text-neutral-400 border-neutral-200 dark:border-zinc-900"
			>
				<div class="flex space-x-2">
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#282828] whitespace-nowrap"
						>Explore other mailing services</span
					>
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#282828] whitespace-nowrap"
						>Explore other mailing services</span
					>
				</div>
				<div class="flex space-x-2">
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#282828] whitespace-nowrap"
						>Follow up: Edition #47</span
					>
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-gray-200 dark:bg-[#282828] whitespace-nowrap"
						>Review: Group idea for collaboration</span
					>
				</div>
			</div>
		</div>
		<!-- Dashkit -->
		<div
			class="px-6 py-4 bg-indigo-100 text-stone-800 dark:text-white dark:bg-transparent"
		>
			<div class="flex items-center justify-between">
				<div class="flex items-center font-semibold">
					<div
						class="inline-flex items-center justify-center w-8 h-8 mr-3 bg-indigo-200 rounded-lg dark:bg-indigo-500"
					>
						<IconMailBolt :size="18" class="text-white" />
					</div>
					Dashkit
				</div>
				<div class="flex items-center text-sm">active last 4 days</div>
			</div>
			<div
				class="w-full h-1.5 mt-2 overflow-hidden rounded-full bg-indigo-200 dark:bg-[#393939]"
			>
				<div
					class="h-1.5 bg-indigo-500 rounded-full ring-2 ring-lime-300 dark:ring-[#282828]"
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

			<!-- Tags -->
			<div
				class="py-4 mt-4 space-y-2 overflow-x-auto text-xs text-indigo-400 border-t border-indigo-200 dark:border-zinc-900"
			>
				<div class="flex space-x-2">
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-indigo-200 dark:bg-[#383838] whitespace-nowrap"
						>Explore other mailing services</span
					>
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-indigo-200 dark:bg-[#383838] whitespace-nowrap"
						>Explore other mailing services</span
					>
				</div>
				<div class="flex space-x-2">
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-indigo-200 dark:bg-[#383838] whitespace-nowrap"
						>Follow up: Edition #47</span
					>
					<span
						class="inline-block px-3 rounded-lg py-1.5 bg-indigo-200 dark:bg-[#383838] whitespace-nowrap"
						>Review: Group idea for collaboration</span
					>
				</div>
			</div>
		</div>
	</div>
</template>
