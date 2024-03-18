<script>
    import Booking from './book_components/booking.svelte';
    import BookingSummary from './book_components/booking_summary.svelte';

    let activeTab = 'booking';
    
     // Function to switch active tab
     function switchTab(tab) {
        activeTab = tab;
    }

    let selectedRoom = '';
    let selectedDateFrom = '';
    let selectedDateTo = '';
    let breakfast = '';
    let dinner = '';
    let lunch = '';
    let none = '';

</script>

<!-- Render active tab content -->
{#if activeTab === 'booking'}
    <div>
        <Booking bind:selectedRoom={selectedRoom}
                 bind:selectedDateFrom={selectedDateFrom}
                 bind:selectedDateTo={selectedDateTo}
                 bind:breakfast={breakfast}
                 bind:lunch={lunch}
                 bind:dinner={dinner}
                 bind:none={none}
        />
        <div class="flex justify-center mb-3">
            <button class="{activeTab === 'booking' ? 'bg-yellow-300' : 'bg-white'} 
                bg-yellow-500 hover:bg-yellow-600 text-white py-2 px-6 rounded-full tracking-wide font-bold shadow-lg inline-block"
                on:click={() => { 
                    switchTab('booking_summary');
                }}>
                Confirm Your Choices
            </button>
        </div>
    </div>
{:else if activeTab === 'booking_summary'}
    <div class="py-8">
        <BookingSummary selectedRoom={selectedRoom} selectedDateFrom={selectedDateFrom} selectedDateTo={selectedDateTo} breakfast={breakfast} lunch={lunch} dinner={dinner} none={none} />
    </div>
{/if}
