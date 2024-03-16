<script>
    export let selectedRoom = '';
    export let selectedDateFrom = '';
    export let selectedDateTo = '';
    export let breakfast;
    export let lunch;
    export let dinner;

</script>
<section class="py-8">
    <h2 class="text-3xl font-semibold mb-8 text-center">Reservation Summary</h2>
    
    <div class="flex flex-col items-center mb-8">
        <p class="font-semibold mb-8 text-center">
            FROM: <span class="text-blue-600">{selectedDateFrom}</span> 
            TO: <span class="text-blue-600">{selectedDateTo}</span>
        </p>
        
        <div class="flex flex-col items-center mb-8">
            <h3 class="text-xl font-semibold mb-2">Selected Room: <span class = 'text-blue-600'> {selectedRoom}</span></h3>
        </div>
        
        <div class="flex flex-col items-center">
            <p class="font-semibold text-center mb-2">DINING</p>
            <ul class="text-center">
                <li>Breakfast: {breakfast ? 'Yes' : 'No'}</li>
                <li>Lunch: {lunch ? 'Yes' : 'No'}</li>
                <li>Dinner: {dinner ? 'Yes' : 'No'}</li>
            </ul>
        </div>
    </div>

    <p class="text-xl font-semibold mb-8 text-center">Price per Night <span class="text-blue-600">$150</span></p>
</section>


<!-- Thank You Message Section -->
<section class = "py-8">
    <div class="container mx-auto text-center">
        <h2 class="text-3xl font-semibold mb-8">Thank You for Your Interest!</h2>
        <p class="text-lg mb-8">We'll get back to you as soon as possible.</p>
    </div>
</section>
