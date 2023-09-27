<script>
    const experiences = [
        {
            id : 1,
            startdate : 'november 2022',
            endDate : '',
            role : 'junior front end developer',
            company: 'axon information systems',
            duties : 'My duties includes but not limited to building front end applications with mordern web frameworks',
            frameworks : [
                {
                    id : 1,
                    language : 'Svelte'
                },
                {
                    id : 2,
                    language : 'Sveltekit'
                },
                {
                    id : 3,
                    language : 'React'
                },
                {
                    id : 4,
                    language : 'Tailwind'
                },
                {
                    id : 5,
                    language : 'Flowbite'
                },
                {
                    id : 6,
                    language : 'Felte'
                },
                {
                    id : 7,
                    language : 'Yup'
                },
                {
                    id : 8,
                    language : 'Graphql'
                },
                {
                    id : 9,
                    language : 'Typescript'
                },

            ]
        },
        {
            id : 2,
            startdate : 'July 2022',
            endDate : 'november 2022',
            role : 'web developer intern',
            company: 'axon information systems',
            duties : 'Basic duites includes Software testing and building front end web applications',
            frameworks : [
                {
                    id : 1,
                    language : 'HTML'
                },
                {
                    id : 2,
                    language : 'CSS'
                },
                {
                    id : 3,
                    language : 'javascript'
                },
                {
                    id : 4,
                    language : 'Tailwind'
                },
                {
                    id : 5,
                    language : 'Daisy ui'
                },
                {
                    id : 6,
                    language : 'React'
                }

            ]
        },
        {
            id : 3,
            startdate : 'November 2021',
            endDate : 'april 2022',
            location : 'United Kingdom',
            role : 'back end developer intern',
            company: 'tiqniat software solutions',
            duties : 'Basic duites includes testing of APIs, building basic CRUD operations with node and express and software testing',
            frameworks : [
                {
                    id : 1,
                    language : 'node'
                },
                {
                    id : 2,
                    language : 'express'
                },
                {
                    id : 3,
                    language : 'mongo db'
                },
                {
                    id : 4,
                    language : 'postman'
                }

            ]
        }
    ]
</script>


<main class="mt-5">
   
    
    {#each experiences as {id, startdate, endDate, frameworks, role, company, duties, location} (id) }
   <main class="mb-5">
    <h1 class="uppercase flex flex-row gap-x-1 mb-3">
        <h1>{startdate}</h1> -
        {#if endDate}
        <h1>{endDate}</h1>
        {:else}
        <h1>present</h1>
        {/if}
    </h1>
    <div class="flex flex-col uppercase mb-1 font-semibold">
       <h1>{role}</h1>
       <h1>{company}</h1>
    </div>

    <p>{duties}</p>

    {#if location}
    <p>{location}</p>
    {:else}
    <p>Accra, Ghana</p>
    {/if}

    <div class="my-2 flex gap-x-2 gap-y-2 flex-wrap">
       {#each frameworks as  {language, id} (id)}
        <span class="bg-primary-200 p-1 px-2 rounded-[12px] uppercase text-xs font-light dark:text-gray-500">{language}</span>
       {/each}

    </div>
   </main>
    {/each}
</main>

<a href="https://drive.google.com/file/d/10NhGcANg4T-rBV7ZnwPhbQCMCd7OeEuo/view" target="_blank">

    <p>See more on my resume *</p>
</a>