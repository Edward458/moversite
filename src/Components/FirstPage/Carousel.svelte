<script>
    import { faker } from '@faker-js/faker';

    export let images = [faker.image.business(1500,866,true),faker.image.business(1500,866,true),faker.image.business(1500,866,true),faker.image.business(1500,866,true),faker.image.business(1500,866,true)];

    let currentSlide = 0;

    const moveLeft = () => {
        if(currentSlide <= 0)
        {
            currentSlide = images.length - 1;
        }
        else{
            currentSlide--;
        }
        console.log(currentSlide);
    }

    const moveRight = () => {
        if(currentSlide >= images.length - 1)
        {
            currentSlide = 0;
        } 
        else
        {
            currentSlide++;
        }

        console.log(currentSlide);
    }

</script>

<div class='flex gap-x-10 self-center'>
    <!-- Left Arrow -->
    <button class='bg-[#909ab5]/75 hover:bg-[#909ab5] rounded-full w-12 h-12 self-center' on:click={moveLeft}>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 m-auto">
            <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 19.5L3 12m0 0l7.5-7.5M3 12h18" />
        </svg>
    </button>

    {#each images as image}
        {#if images[currentSlide] == image}
            <img src={image} alt='carousel' width="843px" height="475px"/>
        {:else}
            <img class='hidden' src={image} alt='carousel' width="843px" height="475px"/>   
        {/if}
    {/each}

    <!-- Right Arrow -->
    <button class='bg-[#909ab5]/75 hover:bg-[#909ab5] rounded-full w-12 h-12 self-center' on:click={moveRight}>
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 m-auto">
            <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
        </svg> 
    </button>
</div>