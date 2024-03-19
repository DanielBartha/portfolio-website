<script>
    import Navbar from "$lib/components/navbar.svelte";
</script>


<body class="bg-gradient-to-r from-cyan-800 to-cyan-700">
    <div class="flex justify-center items-center h-screen">
        <div id="navBarLeft">
            <Navbar />
            <h1
            
                class="text-4xl font-bold tracking-tight text-slate-200 sm:text-xl">
                Daniel Bartha
            </h1>
            <h2
                class="mt-3 text-lg font-medium tracking-tight text-slate-200 sm:text-xl">
                Wannabe software engineer
            </h2>
            <p class="mt-4 max-w-xs leading-normal">
                I build creative solutions for the world's problems
            </p>
            <nav class="lg:block">
                <ul class="mt-16 w-max">
                    <li>Home</li>
                    <li>About</li>
                    <li>Projects</li>
                    <li>Skills</li>
                    <li>Contact</li>
                </ul>
            </nav>
        </div>

        <div id="aboutMe" class="mx-72">
            <p>
                Hey there! I'm Daniel, currently pursuing my Bachelor's in
                HBO-ICT. Passionate about technology with a thirst for knowledge
                and eager to apply my skills in real-world settings. I am
                thriving to create solutions to problems via lines of code. Open
                to networking and exploring opportunities in ICT. Let's connect!
            </p>
        </div>
    </div>
</body>
