<script>
  let name = '';
  let email = '';
  let message = '';
  let reason = '';
  
  function handleSubmit() {
    // Validate form inputs before submission
    if (name.trim() === '' || email.trim() === '' || message.trim() === '') {
      alert('Please fill out all fields.');
      return;
    }

    // Form submission logic
    console.log('Form submitted:', { name, email, message });

    // Clear form fields after submission
    name = '';
    email = '';
    message = '';
  }

</script>

<!-- Banner -->
<section class="hero relative bg-cover bg-center" style="background-image: url('images/room-banner.jpg');">
    <div class="absolute inset-0 bg-black opacity-50"></div> <!-- semi-transparent overlay -->
    <div class="container mx-auto text-center relative z-10 py-20">
        <h2 class="text-4xl font-bold text-white mb-4">About us</h2>
        <p class="text-lg text-white mb-8">Step into a world of refined elegance and comfort as we invite you to explore our luxurious hotel rooms, where every moment is tailored to exceed your expectations.</p>
        <a href="book" class="bg-yellow-500 hover:bg-yellow-600 text-white py-2 px-6 rounded-full tracking-wide font-bold shadow-lg inline-block">Book Now</a>
    </div>
</section>

<div class = "py-8 justify-center">
    <div class="bg-gray-100 rounded-lg shadow-md p-6 max-w-md mx-auto">
    <h2 class="text-2xl font-semibold mb-4">Contact Us</h2>
    <form on:submit|preventDefault={handleSubmit}>
        <div class="mb-4">
        <label for="name" class="block text-sm font-medium mb-1">Name:</label>
        <input type="text" id="name" bind:value={name} class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:border-blue-400" placeholder="Your name">
        </div>
        <div class="mb-4">
        <label for="email" class="block text-sm font-medium mb-1">Email:</label>
        <input type="email" id="email" bind:value={email} class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:border-blue-400" placeholder="Your email">
        </div>
         <div class="mb-4">
        <label for="reason" class="block text-sm font-medium mb-1">Reason for Contact:</label>
            <select id="reason" bind:value={reason} class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:border-blue-400">
                <option value="" disabled selected>Select a Reason</option>
                <option value="booking guidance">Booking Guidance</option>
                <option value="amenities information">Amenities Information</option>
                <option value="food&drinks options">Food & Drinks Options</option>
                <option value="other">Other</option>
            </select>
        </div>
        <div class="mb-4">
        <label for="message" class="block text-sm font-medium mb-1">Message:</label>
        <textarea id="message" bind:value={message} class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:border-blue-400" rows="6" placeholder="Your message"></textarea>
        </div>
        <button type="submit" class="w-full bg-blue-500 hover:bg-blue-600 text-white font-semibold py-2 px-4 rounded-md">Submit</button>
    </form>
    </div>
</div>
