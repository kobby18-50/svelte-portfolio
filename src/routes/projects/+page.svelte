<script>
	import { Heading } from "flowbite-svelte";
    // import Icon from 'flowbite-svelte-icons'
    // import Icon from '@iconify/svelte';

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
                    title : 'Jobsearch'
                },

            ],

            github : 'https://github.com/kobby18-50/react-job-search',
            web : 'https://react-job-search.vercel.app/'
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
            web : 'https://svelte-library-auth-3-0.vercel.app/'
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

    <p class='font-medium mt-5'>Personal Projects</p>

  <div class="grid gap-5">
    {#each personalProjects as project  (project.id) }
   <section class="mt-5">
    <div class="flex justify-between mb-2">
        <h1 class="uppercase">{project.title}</h1>
        <div class="flex space-x-3 mt-2">
            <span><a href={project.github} target="_blank"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5c.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34c-.46-1.16-1.11-1.47-1.11-1.47c-.91-.62.07-.6.07-.6c1 .07 1.53 1.03 1.53 1.03c.87 1.52 2.34 1.07 2.91.83c.09-.65.35-1.09.63-1.34c-2.22-.25-4.55-1.11-4.55-4.92c0-1.11.38-2 1.03-2.71c-.1-.25-.45-1.29.1-2.64c0 0 .84-.27 2.75 1.02c.79-.22 1.65-.33 2.5-.33c.85 0 1.71.11 2.5.33c1.91-1.29 2.75-1.02 2.75-1.02c.55 1.35.2 2.39.1 2.64c.65.71 1.03 1.6 1.03 2.71c0 3.82-2.34 4.66-4.57 4.91c.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2Z"/></svg></span>
            <!-- <span><a href={project.github} target="_blank"><Icon icon="mdi:web" class='text-gray-500 dark:text-gray-500 hover:bg-primary-200 rounded-full' /></span> -->
            {#if project.web}
            <span><a href={project.web} target="_blank"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M16.36 14c.08-.66.14-1.32.14-2c0-.68-.06-1.34-.14-2h3.38c.16.64.26 1.31.26 2s-.1 1.36-.26 2m-5.15 5.56c.6-1.11 1.06-2.31 1.38-3.56h2.95a8.03 8.03 0 0 1-4.33 3.56M14.34 14H9.66c-.1-.66-.16-1.32-.16-2c0-.68.06-1.35.16-2h4.68c.09.65.16 1.32.16 2c0 .68-.07 1.34-.16 2M12 19.96c-.83-1.2-1.5-2.53-1.91-3.96h3.82c-.41 1.43-1.08 2.76-1.91 3.96M8 8H5.08A7.923 7.923 0 0 1 9.4 4.44C8.8 5.55 8.35 6.75 8 8m-2.92 8H8c.35 1.25.8 2.45 1.4 3.56A8.008 8.008 0 0 1 5.08 16m-.82-2C4.1 13.36 4 12.69 4 12s.1-1.36.26-2h3.38c-.08.66-.14 1.32-.14 2c0 .68.06 1.34.14 2M12 4.03c.83 1.2 1.5 2.54 1.91 3.97h-3.82c.41-1.43 1.08-2.77 1.91-3.97M18.92 8h-2.95a15.65 15.65 0 0 0-1.38-3.56c1.84.63 3.37 1.9 4.33 3.56M12 2C6.47 2 2 6.5 2 12a10 10 0 0 0 10 10a10 10 0 0 0 10-10A10 10 0 0 0 12 2Z"/></svg></a></span>
            {/if}

            
            
        </div>
        <!-- <div class="flex space-x-3 mt-2">
            <span><a href={project.github} target="_blank"><Icon icon="mdi:github" /></span>
            {#if project.web}
            <span><a href={project.web} target="_blank"><Icon icon="mdi:github" class='text-gray-500 dark:text-gray-500 hover:bg-primary-200 rounded-full' /></a></span>
            {/if}
            
        </div> -->
    </div>

    <p>{project.description}</p>

    <div class='flex space-x-3'>
        {#each project.languages as {id, title}  (id)}
        <p class="bg-primary-200 p-1 px-2 rounded-[12px] uppercase text-xs font-light dark:text-gray-500">{title}</p>
        {/each}
    </div>
</section>
{/each}
  </div>

   


   





</main>