<script>
import { faker } from '@faker-js/faker';

export let serviceTitle = faker.company.name();
export let serviceImage = faker.image.nature(500,700,true);
</script>

<div class='flex justify-center snap-center'>
  <div class="rounded-lg shadow-lg bg-white max-w-sm">
    <a href="#!">
      <img width="400px" height="600px" src={serviceImage} alt=""/>
    </a>
    <div class="p-6">
      <h5 class="text-gray-900 text-xl font-medium mb-2">{serviceTitle}</h5>
      
    </div>
  </div>
</div>