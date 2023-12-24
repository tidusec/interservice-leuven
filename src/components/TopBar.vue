<template>
    <nav class="topbar">
      <router-link to="/" class="topbar-item">Home</router-link>
      <router-link to="/about-us" class="topbar-item">About Us</router-link>
      <router-link to="/events" class="topbar-item">Events</router-link>
      <router-link to="/contact-us" class="topbar-item">Contact Us</router-link>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'TopBar',
  }
  </script>
  
  <style scoped>
  .topbar {
    display: flex;
    justify-content: space-around;
    padding: 10px;
    position: fixed;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    z-index: 100;
    width: auto;
    min-width: 50%;
    max-width: 80%;
  }
  
  .topbar-item {
    text-decoration: none;
    color: var(--color-text);
  }
  </style>