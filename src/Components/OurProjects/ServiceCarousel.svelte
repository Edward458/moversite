<script>
    import ServiceCard from "./ServiceCard.svelte";
    import { faker } from '@faker-js/faker';

    const items = [];

    for(let i = 0; i < 12; i++)
    {
            items.push({
                name:faker.company.name(),
                image:faker.image.nature(500,700,true)
            });
    }

    let mainImage = 0;
    let leftImage = items.length - 1;
    let rightImage = 1;
</script>

<div class='grid grid-flow-col auto-cols-[24%] overflow-x-auto overscroll-x-contain snap-mandatory snap-x'>
    {#each items as item }
        <ServiceCard serviceTitle={item.name} serviceImage={item.image}/>
    {/each}
      </div>