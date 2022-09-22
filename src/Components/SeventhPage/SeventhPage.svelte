<script>
    import { faker } from '@faker-js/faker';

    export let address = `${faker.address.streetAddress()}, ${faker.address.cityName()}, ${faker.address.stateAbbr()} ${faker.address.zipCode()}`;
    export let email = faker.internet.email();
    export let phone = faker.phone.number('(###) ###-####');
</script>

<div class='flex flex-col gap-y-10 ml-10 py-12'>
    <p class='text-4xl font-bold'>Contact Us</p>

    <!-- Contact Information -->
    <div class='flex flex-col gap-y-2'>
        <!--Address-->
        <p>{address}</p>
        <!-- Email and Phone -->
        <div>
            <p>{phone}</p>
            <p>{email}</p>
        </div>
    </div>

    <button class='bg-[#bfbfbf] hover:bg-[#bfbfe3] text-black rounded-full w-32 h-10 text-sm'>GET IN TOUCH</button>

</div>