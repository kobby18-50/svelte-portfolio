<script lang="ts">
	import { Heading } from 'flowbite-svelte';
    // import { Icon } from 'flowbite-svelte-icons'
	import IMG from '../assets/img.png'
	import TextCarousel from './TextCarousel.svelte';
	import Icon from '@iconify/svelte'
	import REACT from '../assets/icons/react.svg'
	import SVELTE from '../assets/icons/svelte-solid.svg'
	import TAILWIND from '../assets/icons/tailwind-outline.svg'
	import NODE from '../assets/icons/node.svg'
	import EXPRESS from '../assets/icons/express.svg'
	import MONGODB from '../assets/icons/mongodb.svg'
	import TYPESCRIPT from '../assets/icons/typescript.svg'

	let visibleItems = 4;

	const toggleShowMore = () => {
		visibleItems += 5;
	};
	const toggleShowLess = () => {
		visibleItems -= 5;
	};

	const skills = [
		{
			id: 1,
			name: 'react-solid',
			caption: 'React.js',
			icon : REACT
		},
		{
			id: 2,
			name: 'react-solid',
			caption: 'Svelte',
			icon : SVELTE
		},
		{
			id: 3,
			name: 'tailwind-solid',
			caption: 'Tailwind CSS',
			icon : TAILWIND
		},
		{
			id: 4,
			name: 'react-solid',
			caption: 'Node',
			icon : NODE
		},
		{
			id: 5,
			name: 'react-solid',
			caption: 'Express',
			icon : EXPRESS
		},
		{
			id: 6,
			name: 'react-solid',
			caption: 'Mongodb',
			icon : MONGODB
		},
		{
			id: 7,
			name: 'react-solid',
			caption: 'Typescript',
			icon : TYPESCRIPT
		}
	];

	
</script>

<main class="flex flex-col sm:flex-row sm:space-x-10">
	<div>
		<figure class="mt-24">
			<img src={IMG} alt="" class="animate-bounce" />
		</figure>
	</div>

	<div>
		<Heading tag="h3" class='pt-2'>Edward Kwabena Tackie</Heading>
		<h1 class="font-semibold pt-2">Software Engineer</h1>
		

		<p class="mt-5">
			I am a Full-Stack Web developer doing Node.js and Express.js, React.js & Svelte/Kit. I love to
			develop things. I'd rather say I am addicted to development and coding
		</p>

		<div class="flex mt-5 flex-wrap gap-x-2 gap-y-3">
			{#each skills.slice(0, visibleItems) as skill (skill.id)}
				<span class="border-2 border-black p-1 rounded-md text-xs flex hover:bg-green-300">
					<span class="flex space-x-2">
						<span>{skill.caption}</span>
						<!-- <span>{skill.icon}</span> -->
						<!-- <span><Icon size='xs' class='mt-0.5' name={skill.name}/></span> -->
						<span><img src={skill.icon} alt=""></span>
					</span>
				</span>
			{/each}

			{#if visibleItems < skills.length}
				<button class="flex space-x-3" on:click={toggleShowMore}>
                    <span>Show more</span>
					<Icon icon="teenyicons:down-outline" width="10" height="10" class='mt-2' />
                <!-- <Icon size='xs' name='chevron-up-outline' class='mt-1.5'/> -->
                </button>
				{:else}
				<button class="flex space-x-3" on:click={toggleShowLess}>
                    <span>Show less</span>
					<Icon icon="teenyicons:up-outline" width="10" height="10" class='mt-2' />
                <!-- <Icon size='xs' name='chevron-down-outline' class='mt-1.5'/> -->
                </button>
				
			{/if}
		</div>
	</div>
</main>
