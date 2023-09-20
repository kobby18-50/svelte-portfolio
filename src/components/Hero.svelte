<script lang="ts">
	import { Heading } from 'flowbite-svelte';
    import { Icon } from 'flowbite-svelte-icons'
	import IMG from '../assets/img.png'
	import TextCarousel from './TextCarousel.svelte';

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
			caption: 'React.js'
		},
		{
			id: 2,
			name: 'react-solid',
			caption: 'Svelte'
		},
		{
			id: 3,
			name: 'tailwind-solid',
			caption: 'Tailwind CSS'
		},
		{
			id: 4,
			name: 'react-solid',
			caption: 'Node'
		},
		{
			id: 5,
			name: 'react-solid',
			caption: 'Express'
		},
		{
			id: 6,
			name: 'react-solid',
			caption: 'Mongodb'
		},
		{
			id: 7,
			name: 'react-solid',
			caption: 'Typescript'
		}
	];

	
</script>

<main class="flex flex-col sm:flex-row sm:space-x-10">
	<div>
		<figure class="mt-14">
			<img src={IMG} alt="" class="animate-bounce" />
		</figure>
	</div>

	<div>
		<Heading tag="h3" class='pt-2'>Hey, Geeks!</Heading>
		<TextCarousel/>
		

		<p class="mt-5">
			I am a Full-Stack Web developer doing Node.js and Express.js, React.js & Svelte/Kit. I love to
			develop things. I'd rather say I am addicted to development and coding
		</p>

		<div class="flex mt-5 flex-wrap space-x-3 gap-y-3">
			{#each skills.slice(0, visibleItems) as skill (skill.id)}
				<span class="border-2 border-black p-1 rounded-md text-xs flex hover:bg-green-300">
					<span class="flex space-x-2">
						<span>{skill.caption}</span>
						<span><Icon size='xs' class='mt-0.5' name={skill.name}/></span>
					</span>
				</span>
			{/each}

			{#if visibleItems < skills.length}
				<button class="flex space-x-3" on:click={toggleShowMore}>
                    <span>Show more</span>
                <Icon size='xs' name='chevron-up-outline' class='mt-1.5'/>
                </button>
				{:else}
				<button class="flex space-x-3" on:click={toggleShowLess}>
                    <span>Show less</span>
                <Icon size='xs' name='chevron-down-outline' class='mt-1.5'/>
                </button>
				
			{/if}
		</div>
	</div>
</main>
