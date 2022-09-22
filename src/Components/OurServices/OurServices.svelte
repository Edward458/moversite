<script>
    import ServiceCard from "./ServiceCard.svelte";


</script>

<div class='bg-[#212020] flex flex-col gap-y-10 py-10'>
    <p class='text-white text-5xl w-1/12 ml-40'>Our Services</p>
    <div class='flex self-center gap-x-4'>
        <ServiceCard/>
        <ServiceCard/>
        <ServiceCard/>
        <ServiceCard/>
    </div>
    <button class='bg-[#bfbfbf] hover:bg-[#bfbfe3] text-black rounded-full w-32 h-10 text-sm ml-40'>GET IN TOUCH</button>
</div>