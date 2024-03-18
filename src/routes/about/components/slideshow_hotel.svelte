
<script>
    import { onMount, onDestroy } from 'svelte';

    let currentIndex = 0;
    let hotel_img = 'images/hotel_3.jpg';

    const hotel_imgs = [
        {
            hotel_img: 'images/hotel_7.jpg',
        },
        {
            hotel_img: 'images/hotel_3.jpg',
        },
        {
            hotel_img: 'images/hotel_8.jpg',
        },
        {
            hotel_img: 'images/hotel_9.jpg',
        },
        {
            hotel_img: 'images/hotel_6.jpg',
        }
    ];

    function next() {
        currentIndex++;
        if (currentIndex >= hotel_imgs.length) {
            currentIndex = 0;
        }
        updateHotelImg();  
    }

    function prev() {
        currentIndex--;
        if (currentIndex < 0) {
            currentIndex = hotel_imgs.length - 1;
        }
        updateHotelImg();
    }

    function updateHotelImg() {
        hotel_img = hotel_imgs[currentIndex].hotel_img;
    }

    // Automatic slideshow
    let intervalId;

    function startSlideshow() {
        intervalId = setInterval(next, 4000); 
    }

    function stopSlideshow() {
        clearInterval(intervalId);
    }

    // Start the slideshow when the component is mounted
    onMount(() => {
        startSlideshow();
    });

    // Stop the slideshow when the component is unmounted
    onDestroy(() => {
        stopSlideshow();
    });
</script>

<!-- Room Cards -->
<div class="container mx-auto items-center">
    <!-- Room Image -->
    <img src={hotel_img} alt="Hotel_Image" class="w-256 h-128 object-cover">
</div>
