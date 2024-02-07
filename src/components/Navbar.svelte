<script>
import { DarkMode, NavLi, NavUl } from "flowbite-svelte";
import {page} from '$app/stores'
</script>


<nav class="flex justify-end mt-2">
    <DarkMode/>
</nav>
<nav class="">
    <div class="">
        <!-- <NavUl ulClass='flex space-x-10'>
            <NavLi href='/'>Home</NavLi>
            <NavLi href='/project'>Projects</NavLi>
            <NavLi href='/experience'>Experience</NavLi>
        </NavUl> -->
        <ul class="justify-center flex mt-3 space-x-10">
            <li class:active={$page.url.pathname === "/"}><a href="/">Home</a></li>
            <li class:active={$page.url.pathname === "/projects" }><a href="/projects">Projects</a></li>
            <li class:active={$page.url.pathname === "/experience"}><a href="/experience">Experience</a></li>
        </ul>
    </div>
</nav>


<style lang="postcss">
    .active{
        font-weight: bolder;
        box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
    }

    .active{
        @apply font-bold
    }
</style>
