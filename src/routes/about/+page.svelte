<script>
    import SlideshowHotel from "./components/slideshow_hotel.svelte";
    import SlideshowParis from "./components/slideshow_paris.svelte";
</script>

<!-- About Section -->
<section class="about py-16 bg-white">
    <div class="container mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-10 items-center">
            <div class="about-content">
                <h2 class="text-3xl font-semibold mb-4">About Our Hotel</h2>
                <p class="text-lg mb-8">At Our Hotel, we strive to provide our guests with exceptional hospitality and unforgettable experiences. Learn more about our story and commitment to excellence.</p>
                <p class="text-lg mb-8">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed commodo risus quis lorem aliquet fermentum. Vivamus nec ex purus. Integer luctus, elit id fermentum fermentum, turpis dolor aliquet sem, non auctor nunc justo eu libero. Curabitur auctor, arcu in aliquet luctus, odio lectus vehicula lectus, sit amet vestibulum felis neque eget risus.</p>
            </div>
            <div class="about-image">
                <!-- Image for About Section -->
                <SlideshowHotel />
            </div>
        </div>
    </div>
</section>

<!-- About the City Section -->
<section class="about pb-16 bg-gray-100 py-8">
    <div class="container mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-10 items-center">
            <div class="about-image">
                <!-- Image for About the City Section -->
                <SlideshowParis />
            </div>
            <div class="about-content">
                <h2 class="text-3xl font-semibold mb-4">About the City</h2>
                <p class="text-lg mb-8">Discover the vibrant culture and rich history of our city. From iconic landmarks to hidden gems, there's something for everyone to explore.</p>
                <p class="text-lg mb-8">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed commodo risus quis lorem aliquet fermentum. Vivamus nec ex purus. Integer luctus, elit id fermentum fermentum, turpis dolor aliquet sem, non auctor nunc justo eu libero. Curabitur auctor, arcu in aliquet luctus, odio lectus vehicula lectus, sit amet vestibulum felis neque eget risus.</p>
            </div>
        </div>
    </div>
</section>