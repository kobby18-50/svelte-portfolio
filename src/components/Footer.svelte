<script>
    import { Footer, FooterCopyright, FooterLinkGroup, FooterLink, FooterBrand, FooterIcon } from 'flowbite-svelte';
    // import { Icon } from 'flowbite-svelte-icons';
    import Icon from '@iconify/svelte';
  </script>
  
  <Footer footerType="socialmedia">
    
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
    <div class="sm:flex sm:items-center sm:justify-between">
      <FooterCopyright href="/" by="Kobby Industries" />
      <div class="flex mt-4 space-x-6 sm:justify-center sm:mt-0">
        <FooterIcon target='_blank' href="https://www.facebook.com/eddy.blay.161?mibextid=b06tZ0">
          <Icon icon="ri:facebook-line" class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
        </FooterIcon>
        
        <FooterIcon target='_blank' href="https://x.com/ekom_di_garcon?s=21&t=c69uJodHi0XO4sBrX1U3Jg">
          <Icon icon="mdi:twitter" class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
          <!-- <Icon name="twitter-solid" class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" /> -->
        </FooterIcon>
        <FooterIcon target='_blank' href="https://github.com/kobby18-50">
          <Icon icon="mdi:github" class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
          <!-- <Icon name="github-solid" class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" /> -->
        </FooterIcon>
        <FooterIcon target='_blank' href="mailto:edwardkobby18@gmail.com">
          <Icon icon="mdi:gmail" class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
          
        </FooterIcon>
        
      </div>
    </div>
  </Footer>