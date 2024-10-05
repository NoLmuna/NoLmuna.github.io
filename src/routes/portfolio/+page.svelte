<script lang="ts">
	const portfolioImages = [
		{
			alt: "It's for an activity to make your own logo for a site",
			src: "portfolio/activityownlogo.png",
		},
		{
			alt: "Made with adobe photopea because I don't have an adobe photoshop",
			src: "portfolio/adobe photoshop.png",
		},
		{
			alt: "progress report for collage in our app dev",
			src: "portfolio/collage.png",
		},
		{
			alt: "other part of the collage",
			src: "portfolio/collage1.png",
		},
		{
			alt: "It's a php web application",
			src: "portfolio/food-order.png",
		},
        {
			alt: "initial look of what it looks like for the food ordering system",
			src: "portfolio/food ordering system.png",
		},
        {
			alt: "initial look of what it looks like for the food ordering system",
			src: "portfolio/food ordering system1.png",
		},
        {
			alt: "initial look of what it looks like for the food ordering system",
			src: "portfolio/food ordering system2.png",
		},
        {
			alt: "initial look of what it looks like for the food ordering system",
			src: "portfolio/food ordering system3.png",
		},
        {
			alt: "initial look of what it looks like for the food ordering system",
			src: "portfolio/food ordering system4.png",
		},
	];
</script>

<h1 class="text-4xl text-center">Portfolio</h1>
<p class="text-center mb-8">Here are the images that I can salvage from the past years that I have worked on:</p>
<div class="w-full max-w-4xl mx-auto">
    <div class="grid gap-8 grid-cols-1 md:grid-cols-2">
        {#each portfolioImages as portfolioImage (portfolioImage.src)}
        <div class="w-full h-fit overflow-hidden rounded-lg text-center">
            <!-- Image -->
            <img 
                src={portfolioImage.src} 
                alt={portfolioImage.alt} 
                class="w-full h-80 object-contain hover:scale-110 transition-transform duration-300 mx-auto" 
                loading="lazy"
            >
            <!-- Description -->
            <p class="mt-4 text-lg">{portfolioImage.alt}</p>
        </div>
        {/each}
    </div>
</div>

