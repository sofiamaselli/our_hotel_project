<script>
  import RoomCards from './home_components/RoomCards.svelte';
</script>

<!-- Welcome Section -->
<section class="hero relative bg-cover bg-center" style="background-image: url('src/images/lobby.jpg');">
    <div class="absolute inset-0 bg-black opacity-50"></div> <!-- semi-transparent overlay -->
    <div class="container mx-auto text-center relative z-10 py-20">
        <h2 class="text-4xl font-bold text-white mb-4">Welcome to Our Hotel</h2>
        <p class="text-lg text-white mb-8">Experience luxury and comfort at our exquisite hotel.</p>
        <a href="book" class="bg-yellow-500 hover:bg-yellow-600 text-white py-2 px-6 rounded-full tracking-wide font-bold shadow-lg inline-block">Book Now</a>
        <!-- Here Search Bar with Dates instead of Book Now -->
    </div>
</section>


<!-- About Section -->
<section class="about py-16">
    <div class="container mx-auto text-center">
        <h2 class="text-3xl font-bold mb-4">About Us</h2>
        <p class="text-lg mb-8">Discover the elegance and charm of Our Hotel. We offer luxurious accommodations, exceptional dining experiences, and unparalleled hospitality.</p>
        <a href="about" class="text-gray-600 hover:underline">More About Us</a>
    </div>
</section>

<!-- Rooms Section -->
<section class="featured-rooms pb-16">
    <div class="container mx-auto text-center">
        <h2 class="text-3xl font-bold mb-4">Our Rooms</h2>
        <a href = "rooms" class="text-gray-600 hover:underline">Find out more </a>
    </div>
    <RoomCards />
    </section>

<!-- Contacts Section -->
<section class="about pb-16 text-center">
    <h2 class="text-3xl font-bold mb-4 mx-auto">Contacts</h2>
    <p class="text-lg mb-8 mx-auto flex flex-col items-center">
        <span>Phone: +33 6 12 34 56 78</span>
        <span>Email: ourhotel@ourhotel.com</span>
        <span>Address: 123 Rue de la Université, Paris</span>
    </p>
    <div class="flex justify-center">
        <img src="src/images/Map.png" alt="Map" class="w-256 rounded-lg shadow-lg pb-10">
    </div>
</section>


