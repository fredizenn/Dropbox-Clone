<script>

	import { Button } from "$lib/components/ui/button";
	import { ArrowRight } from "lucide-svelte";

</script>
<div class="bg-[#1e1919]">
    <div class="text-white text-center pt-[72px] max-w-[777px] mx-auto">
        <h1 class="text-3xl md:text-6xl">
            securely collaborate on your projects from anywhere
        </h1>
        <p class="text-sm md:text-lg mt-5">
            With Dropbox, you get a full suite of tools designed to help you create, share, manage, and track content more efficiently. Plus, proven cloud storage you can trust.
        </p>
        <Button class="p-6 text-black capitalize font-semibold mt-10">Get Started Now <ArrowRight class="ml-2" /> </Button>
    </div>
    <video class="mt-10" autoplay playsinline loop muted>
        <track kind="captions" />
        <source src="https://aem.dropbox.com/cms/content/dam/dropbox/warp/en-us/dropbox/dbx1-hero-1920x1080.mp4"
        type="video/mp4" />
    </video>
</div>