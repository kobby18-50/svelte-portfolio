<script>
    import { Gallery } from "flowbite-svelte";
    import DICTIONARY from '../../assets/projects/dictionary.png'
    import LIBRARY from '../../assets/projects/library2.png'
    // import LIBRARY from '../../assets/projects/l'

    const images = [
        {   
            id: 1,
            alt : 'dictionary',
            src : DICTIONARY,
            link : 'https://svelte-dictionary-eta.vercel.app'
        },
        {   
            id: 2,
            alt : 'dictionary',
            src : LIBRARY,
            link : 'https://svelte-dictionary-eta.vercel.app'
        }
    ]
</script>


<main>
    <p class="my-5">
        I have worked on a few amount of projects, some being personal and some are for my current employers, using different technologies and frameworks, from small to medium scale projects
    </p>

    <p>Here are some of the projects that I have worked on</p>

    <div class="mt-5 flex space-x-4 flex-wrap">
        <span class="border-2 border-black rounded-md p-1 flex space-x-2">
           <span>
            Svelte Dictionary
           </span>
           <span>
            icon
           </span>
        </span>
        <span class="border-2 border-black rounded-md p-1 flex space-x-2">
           <span>
            Svelte Library
           </span>
           <span>
            icon
           </span>
        </span>
    </div>



    <!-- images -->
    <Gallery class='sm:grid-cols-2 gap-2'>
        {#each images as {src, alt,link,id} (id) }
            <a class="rounded-lg" target="_blank" href={link}>
                <img src={src} alt={alt} class="rounded-lg">
            </a>
        {/each}
    </Gallery>





</main>