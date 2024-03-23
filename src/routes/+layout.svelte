<style>
    @import 'src/routes/global.css';
</style>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.8">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css" rel="stylesheet">
</head>

<!-- Navigation -->
<nav class="bg-blue-500 text-white py-4">
    <div class="container mx-auto flex justify-between items-center">
        <h2 class="text-2xl font-bold">OUR HOTEL</h2>
        <ul class="flex space-x-4">
            <li><a href="/" class="hover:text-gray-300">Home</a></li>
            <li><a href="about" class="hover:text-gray-300">About</a></li>
            <li><a href="rooms" class="hover:text-gray-300">Rooms</a></li>
            <li><a href="contactform" class="hover:text-gray-300">Contact</a></li>
            <li><a href="amenities" class="hover:text-gray-300">Amenities</a></li>
        </ul>
    </div>
</nav>

<slot />

<!-- Footer -->

<footer class="bg-blue-500 text-white bottom-0 left-0 w-full pt-8 fixed">
    <div class="container mx-auto text-center">
        <h2 class="text-lg font-bold">© 2024 OUR HOTEL</h2>
    </div>
</footer>
