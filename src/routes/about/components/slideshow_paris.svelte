<script>
    import { onMount, onDestroy } from 'svelte';

    let currentIndex = 0;
    let paris_img = 'images/paris_1.jpg';

    const paris_imgs = [
        {
            paris_img: 'images/paris_2.jpg',
        },
        {
            paris_img: 'images/paris_1.jpg',
        },
        {
            paris_img: 'images/paris_3.jpg',
        },
        {
            paris_img: 'images/paris_4.jpg',
        },
        {
            paris_img: 'images/paris_5.jpg',
        }
    ];

    function next() {
        currentIndex++;
        if (currentIndex >= paris_imgs.length) {
            currentIndex = 0;
        }
        updateParisImg();  
    }

    function prev() {
        currentIndex--;
        if (currentIndex < 0) {
            currentIndex = paris_imgs.length - 1;
        }
        updateParisImg();
    }

    function updateParisImg() {
        paris_img = paris_imgs[currentIndex].paris_img;
    }

    // Automatic slideshow
    let intervalId;

    function startSlideshow() {
        intervalId = setInterval(next, 5000); 
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

<!-- Paris -->
<div class="container mx-auto items-center">
    <!-- Paris Image -->
    <img src={paris_img} alt="Paris_Image" class="w-256 h-128 object-cover">
</div>
