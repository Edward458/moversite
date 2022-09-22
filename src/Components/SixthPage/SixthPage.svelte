<script>
    import { faker } from '@faker-js/faker';

    const testimonies = [];

    for(let i = 0; i < 5; i++)
    {
        testimonies.push({
            review: faker.lorem.sentences(3),
            customer: faker.name.fullName()
        })
    }

    let currentTestimony = 0;

    const moveLeft = () => {
        if(currentTestimony <= 0)
        {
            currentTestimony = testimonies.length - 1;
        }
        else
        {
            currentTestimony--;
        }
    }

    const moveRight = () => {
        if(currentTestimony >= testimonies.length - 1)
        {
            currentTestimony = 0;
        }
        else
        {
            currentTestimony++;
        }
    }
</script>

<div class='bg-[#2547a0] text-white flex flex-col items-center gap-y-10 py-12'>
    <!-- Header -->
    <p class='text-4xl font-bold'>What Our Clients Say</p>

    <!-- Testimony -->
    <ul class='w-1/2 flex flex-col items-center gap-y-2'>
        {#each testimonies as testimony}
            {#if testimonies[currentTestimony] == testimony}
                <li class='flex flex-col items-center h-24'>
                    <!-- Review -->
                    <p class='text-lg font-bold'>{testimony.review}</p>
                    <!-- Customer -->
                    <p class='text-md'>{testimony.customer}</p>
                </li>
            {:else}
                <li class='hidden'>
                    <!-- Review -->
                    <p class='text-lg font-bold'>{testimony.review}</p>
                    <!-- Customer -->
                    <p class='text-md'>{testimony.customer}</p>
                </li>
            {/if}
        {/each}
    </ul>

    <!-- Buttons -->
    <div class='flex gap-x-4'>
            <!-- Left Arrow -->
            <button class='bg-[#909ab5]/75 hover:bg-[#909ab5] rounded-full w-12 h-12 self-center' on:click={moveLeft}>
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 m-auto">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 19.5L3 12m0 0l7.5-7.5M3 12h18" />
                </svg>
            </button>
        
            <!-- Right Arrow -->
            <button class='bg-[#909ab5]/75 hover:bg-[#909ab5] rounded-full w-12 h-12 self-center' on:click={moveRight}>
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 m-auto">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
                </svg> 
            </button>
    </div>
</div>