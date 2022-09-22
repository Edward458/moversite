<script>
    import { faker } from '@faker-js/faker';

    export let logoName = faker.company.bsBuzz();
</script>

<!-- Navbar -->
<div class='flex justify-between text-white bg-[#2547a0] items-center py-6 px-4'>
    <!-- Logo Name -->
    <a href='/'>
        <p class='text-3xl font-extrabold'>{logoName}</p>
    </a>

    <!-- Logos and Buttons -->
    <div class='flex gap-x-12'>
        <a href='https://www.instagram.com/' class='self-center'>
            <i class="fa-brands fa-instagram fa-xl"></i>
        </a>

        <a href='https://www.youtube.com/' class='self-center'>
            <i class="fa-brands fa-youtube fa-xl"></i>
        </a>

        <a href='https://www.facebook.com/' class='self-center'>
            <i class="fa-brands fa-facebook-f fa-xl"></i>
        </a>

        <button class='bg-[#bfbfbf] hover:bg-[#bfbfe3] text-black rounded-full w-32 h-10 text-sm'>GET IN TOUCH</button>
    </div>
</div>