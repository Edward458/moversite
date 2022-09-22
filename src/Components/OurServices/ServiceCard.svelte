<script>
    import { faker } from '@faker-js/faker';

    export let serviceLogo = faker.internet.emoji();
    export let serviceTitle = faker.company.bsNoun();
    export let serviceDescription = faker.commerce.productDescription();
</script>

<div class="flex justify-center">
  <div class="shadow-lg bg-white max-w-sm">
        <p class='text-9xl mb-20 mt-10'>{serviceLogo}</p>
    <div class="p-6">
      <h5 class="text-gray-900 text-xl font-medium mb-2">{serviceTitle}</h5>
      <p class="text-gray-700 text-base mb-4">
       {serviceDescription} 
      </p>
    </div>
  </div>
</div>