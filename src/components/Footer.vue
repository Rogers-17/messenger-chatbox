<script setup lang="ts">
// No script logic needed for this footer component
</script>

<template>
  <!-- Footer dark background -->
  <footer id="contact" class="bg-[#1e293b] text-[#e4eaf2] pt-16 pb-8">
    <!-- Container footer content -->
    <div class="max-w-[1200px] w-full justify-center items-center mx-auto container">
      
      <div class="grid grid-cols-1 gap-8 mb-12 md:grid-cols-[2fr_1fr_1fr_1fr] md:gap-12">
        <!-- Section 1: Brand info and social links -->
        <div class="footer-section">
          <!-- Company logo -->
          <img class="nav-logo-img w-20 h-20" src="../../public/arro-chat-bot.png" alt="">
          <!-- Brand description -->
          <p class="footer-description">
            Empowering businesses with intelligent chatbot solutions for better customer engagement.
          </p>
          <!-- Social media links with FontAwesome icons -->
          <div class="flex gap-4">
            <!-- Facebook link -->
            <a href="https://web.facebook.com/" class="social-link ">
               <i class="fa-brands fa-facebook text-white text-2xl"></i>
            </a>
            <!-- Twitter/X link -->
            <a href="https://x.com/" class="social-link">
              <i class="fa-brands fa-twitter text-white text-2xl"></i>
            </a>
            <!-- LinkedIn link -->
            <a href="https://www.linkedin.com/" class="social-link">
              <i class="fa-brands fa-linkedin text-white text-2xl"></i>
            </a>
          </div>
        </div>

        <!-- Section 2: Product links -->
        <div class="footer-section">
          <h4 class="text-lg font-semibold text-white mb-6">Product</h4>
          <ul class="footer-links">
            <li><a href="#features">Features</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Integrations</a></li>
            <li><a href="#">API</a></li>
          </ul>
        </div>

        <!-- Section 3: various pages links -->
        <div class="footer-section">
          <h4 class="text-lg font-semibold text-white mb-6">Company</h4>
          <ul class="footer-links">
            <li><a href="#">About Us</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Careers</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </div>

        <!-- Section 4: Support links -->
        <div class="footer-section">
          <h4 class="text-lg font-semibold text-white mb-6">Support</h4>
          <ul class="footer-links">
            <li><a href="#">Help Center</a></li>
            <li><a href="#faqs">FAQs</a></li>
            <li><a href="#">Documentation</a></li>
            <li><a href="#">Community</a></li>
          </ul>
        </div>
      </div>

      <!-- copyright and legal links -->
      <div class="pt-8 border-t border-slate-800 flex justify-between items-center flex-wrap gap-4  ">
        <!-- Copyright notice -->
        <p class="text-gray-400 m-0 ">&copy; 2025 <span class="text-blue-500">ArRo ChatBot.</span> All rights reserved.</p>
        <!-- Legal links: Privacy and Terms -->
        <div class="flex gap-2 text-slate-400 no-underline transition-colors duration-300">
          <a class="hover:text-blue-700" href="#">Privacy Policy</a>
          <a class="hover:text-blue-700" href="#">Terms of Service</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<!-- custom styles for Footer component -->
<style scoped>
/* Footer description text*/
.footer-description {
  color: #94a3b8;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

/* Social media links*/
.social-link {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: #334155;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #e2e8f0;
  transition: all 0.3s ease;
}

/* Social link hover*/
.social-link:hover {
  background-color: #2563eb;
  transform: translateY(-3px);
}

/* Footer links list*/
.footer-links {
  list-style: none;
  padding: 0;
  margin: 0;
}

/* Footer link items*/
.footer-links li {
  margin-bottom: 0.75rem;
}

/* Footer links */
.footer-links a {
  color: #94a3b8;
  text-decoration: none;
  transition: color 0.3s ease;
}

/* Footer links hover changes to blue */
.footer-links a:hover {
  color: #2563eb;
}
</style>
