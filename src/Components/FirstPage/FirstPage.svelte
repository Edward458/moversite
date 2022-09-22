<script>
    import { faker } from '@faker-js/faker';
    import Carousel from './Carousel.svelte';

    export let tagLine = faker.company.catchPhrase();
</script>

<div class='bg-[#2547a0] flex flex-col pb-10 gap-y-4'>
    <p class='text-white text-6xl font-extrabold w-1/4 self-end pr-10'>{tagLine}</p>

    <Carousel/>
</div>