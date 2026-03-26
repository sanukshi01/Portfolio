<template>
  <div class="contact-container">
    <!-- Contact Information Section -->
    <div class="contact-info-section">
      <div class="section-header">
        <h2 class="section-title">Contact Information</h2>
      </div>
      
      <div class="info-grid">
        <div class="info-card">
          <div class="info-icon email-icon">📧</div>
          <div class="info-content">
            <div class="info-label">Email</div>
            <div class="info-value">sanukshikapuvanasingam@gmail.com</div>
          </div>
        </div>

        <div class="info-card">
          <div class="info-icon phone-icon">📞</div>
          <div class="info-content">
            <div class="info-label">Phone</div>
            <div class="info-value">0741451624</div>
          </div>
        </div>

        <div class="info-card">
          <div class="info-icon location-icon">📍</div>
          <div class="info-content">
            <div class="info-label">Location</div>
            <div class="info-value">Trincomalee</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Ready to Start Career Section -->
    <div class="career-section">
      <div class="section-header">
        <h2 class="section-title">Ready to Start My Career</h2>
      </div>
      <p class="career-description">
        As a fresher, I'm actively seeking opportunities to begin my professional journey. 
        Whether it's a full-time position, internship, or freelance project, I'm eager to 
        learn, contribute, and prove myself. Open to entry-level roles in web development.
      </p>
    </div>

    <!-- Your existing contact form (optional - can be removed if not needed) -->
    <div class="form-section" v-if="showForm">
      <h3 class="form-title">Get In Touch</h3>
      <form @submit.prevent="submitForm" class="contact-form">
        <input v-model="name" type="text" placeholder="Your Name" required />
        <input v-model="email" type="email" placeholder="Your Email" required />
        <textarea v-model="message" placeholder="Your Message" required></textarea>
        <button type="submit">Send Message</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage',
  data() {
    return {
      showForm: true, // Set to false if you don't want the form
      name: "",
      email: "",
      message: "",
    };
  },
  methods: {
    submitForm() {
      alert(`Thank you ${this.name}, your message has been sent!`);
      this.name = this.email = this.message = "";
    },
  },
}
</script>

<style scoped>
.contact-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  background: #f8f9ff;
  min-height: 100vh;
}

.section-header {
  margin-bottom: 2rem;
}

.section-title {
  font-size: 1.75rem;
  font-weight: 700;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 0;
}

/* Contact Information Section */
.contact-info-section {
  background: rgba(139, 92, 246, 0.05);
  border-radius: 20px;
  padding: 2.5rem;
  margin-bottom: 2rem;
  border: 1px solid rgba(139, 92, 246, 0.2);
}

.info-grid {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.info-card {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.5rem;
  background: rgba(255, 255, 255, 0.7);
  border-radius: 16px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  transition: all 0.3s ease;
}

.info-card:hover {
  transform: translateX(8px);
  box-shadow: 0 8px 25px rgba(139, 92, 246, 0.15);
}

.info-icon {
  font-size: 1.5rem;
  width: 48px;
  height: 48px;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  flex-shrink: 0;
}

.email-icon {
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
}

.phone-icon {
  background: linear-gradient(135deg, #10b981, #34d399);
}

.location-icon {
  background: linear-gradient(135deg, #f59e0b, #fbbf24);
}

.info-content {
  flex: 1;
}

.info-label {
  font-size: 0.9rem;
  color: #6b7280;
  font-weight: 500;
  margin-bottom: 0.25rem;
}

.info-value {
  font-size: 1.1rem;
  font-weight: 600;
  color: #1f2937;
}

/* Career Section */
.career-section {
  background: white;
  border-radius: 20px;
  padding: 2.5rem;
  border: 1px solid #e5e7eb;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
}

.career-description {
  font-size: 1.1rem;
  color: #4b5563;
  line-height: 1.7;
  margin: 0;
}

/* Optional Form Section */
.form-section {
  margin-top: 3rem;
  padding: 2rem;
  background: rgba(139, 92, 246, 0.05);
  border-radius: 20px;
  border: 1px solid rgba(139, 92, 246, 0.2);
}

.form-title {
  font-size: 1.5rem;
  font-weight: 600;
  color: #1f2937;
  margin-bottom: 1.5rem;
  text-align: center;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  max-width: 500px;
  margin: 0 auto;
}

.contact-form input,
.contact-form textarea {
  padding: 1rem 1.25rem;
  border: 2px solid #e5e7eb;
  border-radius: 12px;
  font-size: 1rem;
  transition: all 0.3s ease;
  background: white;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: none;
  border-color: #8b5cf6;
  box-shadow: 0 0 0 3px rgba(139, 92, 246, 0.1);
}

.contact-form textarea {
  resize: vertical;
  min-height: 120px;
}

.contact-form button {
  padding: 1rem 2rem;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
  color: white;
  border: none;
  border-radius: 12px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
}

.contact-form button:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(139, 92, 246, 0.3);
}

/* Responsive Design */
@media (max-width: 768px) {
  .contact-container {
    padding: 1rem;
  }
  
  .contact-info-section,
  .career-section {
    padding: 2rem 1.5rem;
  }
  
  .info-card {
    padding: 1.25rem;
    flex-direction: column;
    text-align: center;
  }
  
  .info-icon {
    margin-bottom: 0.5rem;
  }
}

@media (max-width: 480px) {
  .section-title {
    font-size: 1.5rem;
  }
  
  .info-value {
    font-size: 1rem;
  }
}
</style>