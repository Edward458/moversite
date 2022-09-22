<script>
    import { faker } from '@faker-js/faker';

    const people = [];

    for(let i = 0; i < 4; i++)
    {
        people.push(
            {
                name: faker.name.fullName(),
                jobTitle: faker.name.jobTitle(),
                image: faker.image.people(500,600,true)

            }
        )
    }

</script>

<div class='flex flex-col gap-y-12 py-12'>
    <!-- Header -->
    <div class='text-5xl w-1/12 ml-10'>Our Team</div>
    <!-- People Cards -->
    <ul class='flex justify-center gap-x-4'>
        {#each people as person}
            <li>
                <img src={person.image} alt='person' width="442px" height="590"/>
                <p class='text-xl font-bold'>{person.name}</p>
                <p class='font-light'>{person.jobTitle}</p>
            </li>
        {/each}
    </ul>
</div>