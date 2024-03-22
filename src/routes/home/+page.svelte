<script>
    import Navbar from "$lib/components/Navbar.svelte";
    import Content from "$lib/components/Content.svelte";
    import ProjectScroll from "$lib/components/ProjectScroll.svelte";
</script>

<section class="bg-gradient-to-r from-cyan-950 to-emerald-950">
    <Navbar />
    <ProjectScroll />
    <div class="flex justify-center items-center h-screen">
        <div class="flex">
            <Content />
        </div>
    </div>
</section>
