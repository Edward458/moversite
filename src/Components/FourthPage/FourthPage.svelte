<script>
    import { faker } from '@faker-js/faker';

    export let image = faker.image.city(500,600);
    export let headerLine = faker.company.catchPhrase();
    export let descriptionText = faker.lorem.paragraph();
</script>

<div class='bg-[#2547a0] flex justify-center gap-x-20 py-12'>
    <!-- Image -->
    <img src={image} alt='fourth' width="367px" height="465px" />

    <!-- Text -->
    <div class='text-white w-1/3 self-center grid gap-y-6'>
        <p class='text-3xl font-bold'>{headerLine}</p>
        <p class='text-md'>{descriptionText}</p>
        <button class='bg-[#bfbfbf] hover:bg-[#bfbfe3] text-black rounded-full w-32 h-10 text-sm'>GET IN TOUCH</button>
    </div>
</div>