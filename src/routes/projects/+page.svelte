<script>
	import { Heading } from "flowbite-svelte";
    import { Icon } from 'flowbite-svelte-icons'

    const personalProjects = [
        {
            id : 1,
            title : 'WDWR',
            description : 'A job listing application built as a personal project. Search for jobs, and apply!',
            languages : [
                {
                    id : 1,
                    title : 'React'
                },
                {
                    id : 2,
                    title : 'Typescript'
                },
                {
                    id : 3,
                    title : 'Tailwindcss'
                },
                {
                    id : 4,
                    title : 'Jobsearch api'
                },

            ],

            github : 'https://github.com/kobby18-50/react-job-search',
            web : ''
        },

        {
            id : 2,
            title : 'library application (VIEW)',
            description : 'A basic but intensive library app with user login, registeration and CRUD functionalities',
            languages : [
                {
                    id : 1,
                    title : 'Svelte'
                },
                {
                    id : 2,
                    title : 'Typescript'
                },
                {
                    id : 3,
                    title : 'Tailwindcss'
                }
            ],

            github : 'https://github.com/kobby18-50/svelte-library-auth-3.0',
            web : ''
        },

        {
            id : 3,
            title : 'library application (MC)',
            description : 'A basic but intensive library app with user login, registeration and CRUD functionalities',
            languages : [
                {
                    id : 1,
                    title : 'Node'
                },
                {
                    id : 2,
                    title : 'Express'
                },
                {
                    id : 3,
                    title : 'Mongodb'
                }
            ],

            github : 'https://github.com/kobby18-50/node_express_library3.0',
            web : ''
        },
        {
            id : 3,
            title : 'Dictionary app',
            description : 'A library app that can be viewed on different screens',
            languages : [
                {
                    id : 1,
                    title : 'Svelte'
                },
                {
                    id : 2,
                    title : 'Typescript'
                },
                {
                    id : 3,
                    title : 'Tailwindcss'
                },
               

            ],

            github : 'https://github.com/kobby18-50/svelte-dictionary',
            web : 'https://svelte-dictionary-eta.vercel.app'
        },
    ]

  

   
</script>


<main>
    <p class="my-5">
        I have worked on a few amount of projects, some being personal and some are for my current employers, using different technologies and frameworks, from small to medium scale projects
    </p>

    <p>Here are some of the projects that I have worked on</p>

    <p class='font-medium'>Personal Projects</p>

  <div class="grid gap-5">
    {#each personalProjects as project  (project.id) }
   <section class="mt-5">
    <div class="flex justify-between">
        <h1 class="uppercase">{project.title}</h1>
        <div class="flex space-x-3">
            <span><a href={project.github} target="_blank"><Icon  name='github-solid'/></a></span>
            {#if project.web}
            <span><a href={project.web} target="_blank"><Icon  name='globe-outline'/></a></span>
            {/if}
        </div>
    </div>

    <p>{project.description}</p>

    <div class='flex space-x-3'>
        {#each project.languages as {id, title}  (id)}
        <p class="bg-primary-200 p-1 rounded-[12px] uppercase text-xs font-light">{title}</p>
        {/each}
    </div>
</section>
{/each}
  </div>

   


   





</main>