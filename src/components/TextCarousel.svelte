<!-- TextCarousel.svelte -->
<script>
    let currentIndex = 0;
    const textItems = [
      "Edward",
      "Kwabena",
      "Tackie",
      // Add more text items as needed
    ];
  
    function nextItem() {
      currentIndex = (currentIndex + 1) % textItems.length;
    }


    function startCarousel() {
    const interval = setInterval(() => {
      nextItem();
    }, 3000); // Change the interval (in milliseconds) as needed
  }

  import { onMount } from "svelte";

  onMount(startCarousel);
  </script>
  
  <div class="carousel">
    <p class="text-xl font-bold">I am {textItems[currentIndex]}</p>
  </div>
  
  
  