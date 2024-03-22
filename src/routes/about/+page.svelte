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
                <p class="text-lg mb-8">In the heart of our city, a visionary architect named Alexander discovered a forgotten gem—an old, weathered building with untapped potential. With boundless determination, he transformed it into our beloved hotel, a testament to his passion for creating unforgettable experiences.</p>
                <p class="text-lg mb-8">Every detail, from the elegant façade to the luxurious interiors, reflects Alexander's commitment to excellence. Each room is a sanctuary, designed to surpass the expectations of our guests and provide a home away from home.</p>
                <p class="text-lg mb-8">Since opening our doors, we've welcomed travelers from around the world, offering them a haven of luxury, hospitality, and endless possibilities. Our mission is simple: to create moments of joy, laughter, and connection that last a lifetime.</p>
                <p class="text-lg mb-8">Join us on this journey, where every stay is a story waiting to be written. Welcome to our hotel.</p>
            </div>
            <div class="about-image">
                <!-- Image for About Section -->
                <SlideshowHotel />
            </div>
        </div>
    </div>
</section>

<!-- About the City Section -->
<section class="about pb-16 bg-gray-100 py-8 pb-40">
    <div class="container mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-10 items-center">
            <div class="about-image">
                <!-- Image for About the City Section -->
                <SlideshowParis />
            </div>
            <div class="about-content">
                <h2 class="text-3xl font-semibold mb-4">About the City</h2>
                <p class="text-lg mb-8">Discover the vibrant culture and rich history of our city. From iconic landmarks to hidden gems, there's something for everyone to explore.</p>
                <p class="text-lg mb-8">Welcome to Paris, a timeless city of romance, art, and culture. Steeped in history and brimming with charm, Paris captivates visitors with its iconic landmarks, cobblestone streets, and world-renowned cuisine. From the majestic Eiffel Tower to the grandeur of Notre-Dame Cathedral, every corner tells a story of centuries past. </p> 
                <p class="text-lg mb-8">But Paris is not just a city frozen in time; it is a vibrant metropolis where tradition meets modernity. Wander through the bustling streets of Montmartre, where artists once roamed and creativity thrives to this day. Indulge in a leisurely café au lait at a quintessential Parisian café, or explore the chic boutiques of the Marais district. In the evenings, immerse yourself in the glittering lights of the Champs-Élysées or lose yourself in the melodies of a live jazz performance along the Seine.</p> 
                <p class="text-lg mb-8">Paris is a city of endless discovery, where every moment is filled with possibility and enchantment. Welcome to the magic of Paris, where dreams come alive amidst the beauty of the City of Light.</p>
            </div>
        </div>
    </div>
</section>
