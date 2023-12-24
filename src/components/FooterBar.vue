<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; 2024 Interservice Leuven</p>
      <ul class="footer-links">
        <li><a href="/terms-of-service">Terms of Service</a></li>
        <li><a href="/privacy-policy">Privacy Policy</a></li>
        <li><a href="/contact-us">Contact Us</a></li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      isAtBottom: false
    }
  },
  methods: {
    checkScroll() {
      this.isAtBottom = (window.innerHeight + window.scrollY) >= document.body.offsetHeight;
    }
  },
  mounted() {
    window.addEventListener('scroll', this.checkScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.checkScroll);
  }
}
</script>

<style scoped>
.footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #333;
  color: #fff;
  padding: 1rem 0;
  text-align: center;
  left: 0%;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.footer-links {
  list-style: none;
  display: flex;
  gap: 15px;
}

.footer-links a {
  color: #fff;
  text-decoration: none;
}
</style>