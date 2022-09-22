<script>
    import { faker } from '@faker-js/faker';

    export let headerLine = faker.company.catchPhrase();
    export let smallImage = faker.image.business(500,600);
    export let pageText = faker.lorem.paragraph(5);
    export let bigImage = faker.image.business(700,800);
</script>

<div class='flex flex-col items-center gap-y-20 py-12'>
    <!-- Header -->
    <p class='text-4xl font-bold'>{headerLine}</p>
    <!--Images and Text-->
    <div class='flex justify-center gap-x-40'>
    <!-- Small Image and Text-->
        <div class='w-1/3 grid gap-y-20'>
            <img src={smallImage} alt='small' width="367px" height="465px" />
            <div class='grid gap-y-4'>
                <p class=''>{pageText}</p>
                <p class=''>{pageText}</p>
            </div>
        </div>

    <!-- Big Image -->
        <img src={bigImage} alt='big' width="681px" height="811px"/>
    </div>
</div>