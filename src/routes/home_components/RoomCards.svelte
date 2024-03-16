    <script>

        let currentIndex = 0;
        let type = 'Room 1';
        let comment = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.';
        let roomimage = 'src/images/room_1.jpg';

         const room_cards = [
            {
                type: 'Room 1',
                comment: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                roomimage: 'src/images/room_1.jpg',
            },
            {
                type: 'Room 2',
                comment: 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
                roomimage: 'src/images/room_2.jpg',
            },
            {
                type: 'Room 3',
                comment: 'Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.',
                roomimage: 'src/images/room_3.jpg',
            },
            {
                type: 'Room 4',
                comment: 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
                roomimage: 'src/images/room_4.jpg',
            }
        ];

        function next() {   currentIndex++;
                            if (currentIndex >= room_cards.length) {currentIndex = 0;}
                            updateRoomCard();
                         }

        function prev() {   currentIndex--;
                            if (currentIndex < 0) { currentIndex = room_cards.length - 1;}
                            updateRoomCard();
                        }

        function updateRoomCard() {
                                    type = room_cards[currentIndex].type;
                                    comment = room_cards[currentIndex].comment;
                                    roomimage = room_cards[currentIndex].roomimage;

                                }   
    </script>
    
    

<!-- Room Cards -->
<div class="container mx-auto items-center">
    <div class="relative bg-white shadow-lg rounded-lg overflow-hidden flex flex-col md:flex-row items-center justify-center mx-4">

        <!-- Left Button -->
        <button class="absolute left-0 top-1/2 transform -translate-y-1/2 bg-gray-500 text-white text-xs font-bold focus:outline-none px-2 py-2 rounded-md z-10 ml-5" on:click={prev}>
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/>
            </svg>
        </button>

        <!-- Room Image -->
        <img src={roomimage} alt="{type}" class="w-1/2 h-64 object-cover ml-20 mt-10 mb-10 mr-20">

        <!-- Room Details -->
        <div class="flex flex-col justify-center w-1/2 p-6 mr-20 ml-20">
            <h3 class="text-xl font-semibold mb-2 py-2">{type}</h3>
            <p class="text-gray-600 py-2">{comment}</p>
        </div>

        <!-- Right Button -->
        <button class="absolute right-0 top-1/2 transform -translate-y-1/2 bg-gray-500 text-white text-xs font-bold focus:outline-none px-2 py-2 rounded-md z-10 mr-5" on:click={next}>
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
            </svg>
        </button>
    </div>
</div>
