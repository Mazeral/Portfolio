<script setup>
import { onMounted, onBeforeUnmount } from 'vue';

// Import your view components
import WelcomeView from "./components/WelcomeView.vue";
import AboutView from "./components/AboutView.vue";
import ExperienceView from "./components/ExperienceView.vue";
import FinalView from "./components/FinalView.vue";

// Variable to hold our observer
let observer = null;

// This code runs after the component is added to the page
onMounted(() => {
  // Options for the observer (triggers when 10% of the item is visible)
  const options = {
    root: null, // Use the browser viewport
    rootMargin: '0px',
    threshold: 0.1 // Trigger when 10% is visible (adjust as needed)
  };

  // Create the Intersection Observer
  observer = new IntersectionObserver((entries, observerInstance) => {
    // Loop through each observed element that changed visibility
    entries.forEach(entry => {
      // Check if the element is now intersecting (visible)
      if (entry.isIntersecting) {
        // Add the 'is-visible' class to trigger the CSS animation
        entry.target.classList.add('is-visible');
        // Optional: Stop watching this element after it becomes visible (animate only once)
        observerInstance.unobserve(entry.target);
      }
      // You could add an 'else' here to remove 'is-visible' if you want
      // the animation to reverse when scrolling out of view, but we'll keep it simple.
    });
  }, options);

  // Find all elements we want to animate (add the class 'animate-on-scroll' in the template below)
  const elementsToAnimate = document.querySelectorAll('.animate-on-scroll');

  // Tell the observer to watch each of these elements
  elementsToAnimate.forEach(el => {
    observer.observe(el);
  });
});

// Clean up the observer when the component is removed
onBeforeUnmount(() => {
  if (observer) {
    observer.disconnect();
  }
});
</script>

<template>
  <main>
    <WelcomeView class="animate-on-scroll view-section" />
    <AboutView class="animate-on-scroll view-section" />
    <ExperienceView class="animate-on-scroll view-section" />
    <FinalView class="animate-on-scroll view-section" />
  </main>
</template>

<style scoped>
/* --- CSS for Scroll Animation --- */

/* This is the INITIAL state (before scrolling into view) */
.animate-on-scroll {
  opacity: 0; /* Start fully transparent */
  transform: translateY(40px); /* Start slightly lower */
  transition: opacity 0.6s ease-out, transform 0.6s ease-out; /* Define the smooth animation */
  will-change: opacity, transform; /* Optimization hint for the browser */
}

/* This class is ADDED BY JAVASCRIPT when the element is visible */
.animate-on-scroll.is-visible {
  opacity: 1; /* Fade it in */
  transform: translateY(0); /* Move it back to original position */
}

/* --- Basic Styling for your Views (Make sure they have height!) --- */
.view-section {
  min-height: 80vh; /* IMPORTANT: Give your views some height! */
  padding: 3rem 1rem;
  margin-bottom: 1rem;
  background-color: #eee; /* Example background */
  border: 1px solid #ddd; /* Example border */
  display: flex; /* Example layout */
  align-items: center; /* Example layout */
  justify-content: center; /* Example layout */
  font-size: 1.5rem; /* Example text */
  box-sizing: border-box;
}
.view-section:nth-child(even) {
    background-color: #f8f8f8;
}

/* Optional: Prevent horizontal scrollbars during animation */
main {
  overflow-x: hidden;
  overflow-y: hidden;
}

/* Example header style */
header {
  height: 50px; background: #333; color: white; padding: 0 1rem;
  position: sticky; top: 0; z-index: 10; display:flex; align-items:center;
}
</style>
