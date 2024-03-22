<script>
    export let selectedRoom = '';
    export let selectedDateFrom = '';
    export let selectedDateTo = '';
    export let breakfast;
    export let lunch;
    export let dinner;
    
  </script>

<!-- Booking Info Section -->
<section class="bookings py-8">
    <div class="container mx-auto">
        <h2 class="text-3xl font-semibold mb-8 text-center">Book Your Stay</h2>
        <form class="max-w-lg mx-auto">
            <!-- First and Last Name  -->
            <div class="flex flex-wrap -mx-3 mb-6">
                <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
                    <label class="block uppercase tracking-wide text-gray-700 text-s font-bold mb-2" for="grid-first-name">First Name</label>
                    <input class="appearance-none block w-full bg-gray-200 text-gray-700 border rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:border-blue-400" id="grid-first-name" type="text" placeholder="John">
                </div>
                <div class="w-full md:w-1/2 px-3">
                    <label class="block uppercase tracking-wide text-gray-700 text-s font-bold mb-2" for="grid-last-name">Last Name</label>
                    <input class="appearance-none block w-full bg-gray-200 text-gray-700 border rounded py-3 px-4 leading-tight focus:outline-none focus:border-blue-400" id="grid-last-name" type="text" placeholder="Doe">
                </div>
            </div>
            <!-- Email Address -->
            <div class="flex flex-wrap -mx-3 mb-6">
                <div class="w-full px-3">
                    <label class="block uppercase tracking-wide text-gray-700 text-s font-bold mb-2" for="grid-email">Email Address</label>
                    <input class="appearance-none block w-full bg-gray-200 text-gray-700 border rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:border-blue-400" id="grid-email" type="email" placeholder="john.doe@example.com">
                </div>
            </div>
            <!-- Room Selection -->
            <div class="mb-6">
                <label class="block uppercase tracking-wide text-gray-700 text-s font-bold mb-2" for="roomSelect">Select Room</label>
                <select bind:value={selectedRoom} id="roomSelect" class=" appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
                    <option value="Deluxe">Deluxe</option>
                    <option value="Family">Family</option>
                    <option value="Executive">Executive</option>
                    <option value="Superior">Superior</option>
                </select>
            </div>
            <!-- Date Selection -->
            <div class="grid grid-cols-2 md:grid-cols-2 lg:grid-cols-2 gap-8">
                <div class="mb-6">
                    <label class="block uppercase tracking-wide text-gray-700 text-s font-bold mb-2" for="datePicker_from">From</label>
                    <input id="datePicker_from" bind:value={selectedDateFrom} type="date" name="datePicker" class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
                </div>
                <div class="mb-6">
                    <label class="block uppercase tracking-wide text-gray-700 text-s font-bold mb-2" for="datePicker_to">To</label>
                    <input id="datePicker_to" bind:value={selectedDateTo} type="date" name="datePicker" class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
                </div>
            </div>
            <!-- Food Options -->
            <div class="mb-6">
                <p class="block uppercase tracking-wide text-gray-700 font-bold mb-2">Dining</p>
                <label class="inline-flex items-center">
                    <input type="checkbox" bind:checked={breakfast} class="form-checkbox h-5 w-5 text-blue-500" name="Breakfast">
                    <span class="text-gray-700 text-s ml-2">Breakfast</span>
                </label>
                <label class="inline-flex items-center ml-6">
                    <input type="checkbox" bind:checked={lunch} class="form-checkbox h-5 w-5 text-blue-500" name="Lunch">
                    <span class="text-gray-700 text-s ml-2">Lunch</span>
                </label>
                <label class="inline-flex items-center ml-6">
                    <input type="checkbox" bind:checked={dinner} class="form-checkbox h-5 w-5 text-blue-500" name="Dinner">
                    <span class="text-gray-700 text-s ml-2">Dinner</span>
                </label>
            </div>


        </form>
    </div>
</section>
