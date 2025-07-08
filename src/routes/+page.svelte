<script lang="ts">
  import { onMount } from 'svelte';
  
  let showMainWebsite = false;
  
  function toggleWebsite() {
    showMainWebsite = !showMainWebsite;
  }
</script>

<svelte:head>
  <title>Natrasnac - Storefront</title>
  <meta name="description" content="Natrasnac Storefront - Premium products and services" />
</svelte:head>

<div class="min-h-screen bg-white">
  {#if !showMainWebsite}
    <!-- Landing Page -->
    <div class="flex flex-col items-center justify-center min-h-screen container-main">
      <div class="text-center space-y-8">
        <h1 class="text-6xl sm:text-8xl font-bold text-black tracking-tight">
          Natrasnac
        </h1>
        
        <p class="text-xl text-gray-600 max-w-md mx-auto">
          Premium storefront coming soon
        </p>
        
        <div class="space-y-6">
          <p class="text-lg text-gray-700">
            For inquiries, contact us at:
          </p>
          
          <a 
            href="mailto:contact@natrasnac.com" 
            class="inline-block text-xl font-medium text-black hover:text-gray-700 transition-colors border-b-2 border-black hover:border-gray-700"
          >
            contact@natrasnac.com
          </a>
        </div>
        
        <!-- <div class="pt-8">
          <button 
            on:click={toggleWebsite}
            class="btn-primary text-lg"
          >
            Enter Website
          </button>
        </div> -->
      </div>
    </div>
  {:else}
    <!-- Main Website -->
    <div class="min-h-screen">
      <!-- Navigation -->
      <nav class="bg-white border-b border-gray-200 sticky top-0 z-50">
        <div class="container-main">
          <div class="flex justify-between items-center h-16">
            <div class="flex items-center space-x-8">
              <h1 class="text-2xl font-bold text-black">Natrasnac</h1>
              
              <div class="hidden md:flex space-x-8">
                <a href="#home" class="text-black hover:text-gray-700 transition-colors">Home</a>
                <a href="#about" class="text-black hover:text-gray-700 transition-colors">About</a>
                <a href="#contact" class="text-black hover:text-gray-700 transition-colors">Contact</a>
              </div>
            </div>
            
            <button 
              on:click={toggleWebsite}
              class="btn-secondary text-sm"
            >
              Back to Landing
            </button>
          </div>
        </div>
      </nav>
      
      <!-- Home Section -->
      <section id="home" class="py-20 bg-white">
        <div class="container-main">
          <div class="text-center space-y-8">
            <h2 class="text-5xl font-bold text-black">Welcome to Natrasnac</h2>
            <p class="text-xl text-gray-600 max-w-2xl mx-auto">
              Your premium storefront destination. Discover quality products and exceptional service.
            </p>
            <div class="flex justify-center space-x-4">
              <button class="btn-primary">Shop Now</button>
              <button class="btn-secondary">Learn More</button>
            </div>
          </div>
        </div>
      </section>
      
      <!-- About Section -->
      <section id="about" class="py-20 bg-gray-50">
        <div class="container-main">
          <div class="max-w-4xl mx-auto text-center space-y-8">
            <h2 class="text-4xl font-bold text-black">About Natrasnac</h2>
            <p class="text-lg text-gray-700 leading-relaxed">
              At Natrasnac, we are committed to providing exceptional products and services to our customers. 
              Our team is dedicated to quality, innovation, and customer satisfaction.
            </p>
            <p class="text-lg text-gray-700 leading-relaxed">
              Founded with a vision to create meaningful connections through premium offerings, 
              we continue to evolve and adapt to meet the needs of our growing community.
            </p>
          </div>
        </div>
      </section>
      
      <!-- Contact Section -->
      <section id="contact" class="py-20 bg-white">
        <div class="container-main">
          <div class="max-w-2xl mx-auto text-center space-y-8">
            <h2 class="text-4xl font-bold text-black">Get In Touch</h2>
            <p class="text-lg text-gray-700">
              Ready to connect? We'd love to hear from you.
            </p>
            
            <div class="space-y-6">
              <div class="p-8 bg-gray-50 rounded-lg">
                <h3 class="text-xl font-semibold text-black mb-4">Contact Information</h3>
                <a 
                  href="mailto:contact@natrasnac.com" 
                  class="inline-block text-lg text-black hover:text-gray-700 transition-colors border-b border-black hover:border-gray-700"
                >
                  contact@natrasnac.com
                </a>
              </div>
              
              <button class="btn-primary">Send Message</button>
            </div>
          </div>
        </div>
      </section>
    </div>
  {/if}
</div>

