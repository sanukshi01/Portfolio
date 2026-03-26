<template>
  <section class="home">
    <div class="container">
      <!-- Animated Background Elements -->
      <div class="floating-shapes">
        <div class="shape shape-1"></div>
        <div class="shape shape-2"></div>
        <div class="shape shape-3"></div>
        <div class="shape shape-4"></div>
      </div>

      <div class="hero-content">
        <div class="greeting">
          <h1 class="hey-there">Hey There,</h1>
          <div class="typing-anim">
            <h2>
              I am <span class="highlight">Sanukshika</span>
            </h2>
          </div>
        </div>

        <p class="description">
          I am a motivated and dedicated diploma student specializing in Information Technology,
          with a strong foundation in programming, web development, and problem-solving. I am
          currently seeking an <span class="highlight">internship opportunity</span> to apply
          my technical skills in a practical environment, learn from industry professionals,
          and contribute to real-world projects.
        </p>

        <div class="cta-section">
          <a
            href="/cv/Sanukshika_Puvanasingam_CV.pdf"
            download="Sanukshika_Puvanasingam_Resume.pdf"
            class="cta-button"
          >
            <span>> Check resume</span>
            <div class="button-glow"></div>
          </a>

          <div class="scroll-indicator">
            <div class="mouse-scroll"></div>
          </div>
        </div>
      </div>

      <!-- Profile Image / Avatar -->
      <div class="profile-image"></div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Home",
  mounted() {
    this.startAnimations();
  },
  methods: {
    startAnimations() {
      // Typing animation
      const text = "I am Sanukshika";
      let i = 0;
      const typeWriter = () => {
        if (i < text.length) {
          document.querySelector('.typing-anim h2').textContent = text.slice(0, i + 1);
          i++;
          setTimeout(typeWriter, 100);
        }
      };
      setTimeout(typeWriter, 500);
    },
  },
};
</script>

<style scoped>
.home {
  min-height: 100vh;
  display: flex;
  align-items: center;
  background: linear-gradient(135deg, #0f0f23 0%, #1a0f2e 50%, #2a1a4d 100%);
  position: relative;
  overflow: hidden;
  padding: 0 2rem;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

.home::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 20% 80%, rgba(139, 92, 246, 0.3) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(59, 130, 246, 0.3) 0%, transparent 50%),
    radial-gradient(circle at 40% 40%, rgba(16, 185, 129, 0.2) 0%, transparent 50%);
  z-index: 1;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  position: relative;
  z-index: 2;
  display: flex;
  align-items: center;
  gap: 4rem;
  min-height: 100vh;
}

/* Floating Shapes */
.floating-shapes {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  pointer-events: none;
  z-index: 1;
}

.shape {
  position: absolute;
  border-radius: 50%;
  background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
  animation: float 6s ease-in-out infinite;
}

.shape-1 {
  width: 80px;
  height: 80px;
  top: 20%;
  left: 10%;
  animation-delay: 0s;
}

.shape-2 {
  width: 120px;
  height: 120px;
  top: 60%;
  right: 15%;
  animation-delay: 2s;
}

.shape-3 {
  width: 60px;
  height: 60px;
  bottom: 20%;
  left: 20%;
  animation-delay: 4s;
}

.shape-4 {
  width: 100px;
  height: 100px;
  top: 10%;
  right: 20%;
  animation-delay: 1s;
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(180deg); }
}

/* Hero Content */
.hero-content {
  flex: 1;
  max-width: 600px;
}

.greeting {
  margin-bottom: 2rem;
}

.hey-there {
  font-size: 3rem;
  font-weight: 800;
  background: linear-gradient(135deg, #ffffff, #e5e7eb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 0 0 1rem 0;
  animation: slideInLeft 1s ease-out;
}

.typing-anim h2 {
  font-size: 3.5rem;
  font-weight: 900;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa, #c084fc);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 0;
  animation: slideInLeft 1s ease-out 0.2s both;
}

.highlight {
  position: relative;
}

.highlight::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, #8b5cf6, #a78bfa);
  border-radius: 2px;
  animation: glow 2s ease-in-out infinite alternate;
}

.description {
  font-size: 1.2rem;
  line-height: 1.8;
  color: #d1d5db;
  margin-bottom: 3rem;
  animation: slideInLeft 1s ease-out 0.4s both;
}

.description .highlight {
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  font-weight: 600;
}

/* CTA Section */
.cta-section {
  display: flex;
  align-items: center;
  gap: 2rem;
  animation: slideInLeft 1s ease-out 0.6s both;
}

.cta-button {
  position: relative;
  padding: 1.2rem 2.5rem;
  font-size: 1.1rem;
  font-weight: 700;
  color: white;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
  border: none;
  border-radius: 50px;
  cursor: pointer;
  overflow: hidden;
  transition: all 0.4s ease;
  text-decoration: none; /* important for <a> tag */
}

.cta-button:hover {
  transform: translateY(-4px) scale(1.05);
  box-shadow: 0 20px 40px rgba(139, 92, 246, 0.4);
}

.button-glow {
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(45deg, transparent, rgba(255,255,255,0.3), transparent);
  transform: rotate(45deg);
  transition: all 0.6s ease;
  opacity: 0;
}

.cta-button:hover .button-glow {
  opacity: 1;
  animation: shine 0.6s ease;
}

@keyframes shine {
  0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
  100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
}

.scroll-indicator {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
}

.mouse-scroll {
  width: 30px;
  height: 50px;
  border: 2px solid #8b5cf6;
  border-radius: 25px;
  position: relative;
  animation: scroll 2s infinite;
}

.mouse-scroll::before {
  content: '';
  position: absolute;
  top: 8px;
  left: 50%;
  transform: translateX(-50%);
  width: 6px;
  height: 6px;
  background: #8b5cf6;
  border-radius: 50%;
  animation: scroll-inner 2s infinite;
}

@keyframes scroll {
  0% { opacity: 0; transform: translateY(0); }
  50% { opacity: 1; }
  100% { opacity: 0; transform: translateY(20px); }
}

@keyframes scroll-inner {
  0% { opacity: 0; transform: translateY(0); }
  50% { opacity: 1; }
  100% { opacity: 0; transform: translateY(15px); }
}

/* Profile Image */
.profile-image {
  flex-shrink: 0;
  animation: slideInRight 1s ease-out;
}

/* Animations */
@keyframes slideInLeft {
  from { opacity: 0; transform: translateX(-50px); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes slideInRight {
  from { opacity: 0; transform: translateX(50px); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes glow {
  from { box-shadow: 0 0 5px #8b5cf6; }
  to { box-shadow: 0 0 20px #8b5cf6; }
}

/* Responsive Design */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
    text-align: center;
    gap: 2rem;
    padding: 2rem 1rem;
  }
  
  .hey-there { font-size: 2.5rem; }
  .typing-anim h2 { font-size: 2.8rem; }
  .description { font-size: 1.1rem; }
  .cta-section { flex-direction: column; gap: 1.5rem; }
}

@media (max-width: 480px) {
  .hey-there { font-size: 2rem; }
  .typing-anim h2 { font-size: 2.2rem; }
}
</style>