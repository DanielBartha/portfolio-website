<script>
      // Import Tailwind CSS
      import 'tailwindcss/tailwind.css';
    import { onMount } from 'svelte';

    let highlightStyle = {
    left: '0px',
    top: '0px',
    display: 'none'
};
    let mouseX = 0;
    let mouseY = 0;

    // Function to update highlight position
    function updateHighlightPosition(event) {
    mouseX = event.clientX;
    mouseY = event.clientY;
    highlightStyle = {
        left: `${mouseX -20}px`, // Adjust for half of the width of the highlight
        top: `${mouseY -20}px`, // Adjust for half of the height of the highlight
        display: 'block'
    };
}

    onMount(() => {
        // Run code only on the client side
        if (typeof window !== 'undefined') {
            // Attach mousemove event listener
            window.addEventListener('mousemove', updateHighlightPosition);

            // Cleanup event listener on component destruction
            return () => {
                window.removeEventListener('mousemove', updateHighlightPosition);
            };
        }
    });
</script>

<div class="content-container flex flex-col items-start mx-12">
    <div class="first-content mb-8">
        <h1 class="ml-0 sm:ml-40 text-5xl font-mono tracking-wide text-slate-200 sm:text-xl">
            Daniel Bartha
        </h1>

        <h2 class="ml-0 sm:ml-40 mt-3 text-lg font-mono tracking-wide text-slate-200 sm:text-xl">
            Wannabe software engineer
        </h2>
        
        <p class="ml-0 sm:ml-40 mt-6 text-slate-400 max-w-xs leading-normal">
            I build <i class="underline">creative</i> solutions for the world's problems
        </p>
    </div>

    <div id="aboutMe" class="pt-6 pr-[60rem] pl-24 sm:mx-8 relative">
        <div class="glass-background rounded-lg shadow-2xl">
            <p class="text-white px-5 py-5">
                Hey there! I'm Daniel, currently pursuing my Bachelor's in
                HBO-ICT. Passionate about technology with a thirst for knowledge
                and eager to apply my skills in real-world settings. I am
                thriving to create solutions to problems via lines of code. Open
                to networking and exploring opportunities in ICT. Let's connect!
            </p>
        </div>
    </div>
</div>

<div class="highlight" style="display: {highlightStyle.display}; left: {highlightStyle.left}; top: {highlightStyle.top};"></div>