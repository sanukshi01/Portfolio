<template>
  <div class="about-container">
    <!-- Animated Background Elements -->
    <div class="floating-shapes">
      <div class="shape shape-1"></div>
      <div class="shape shape-2"></div>
      <div class="shape shape-3"></div>
      <div class="shape shape-4"></div>
    </div>

    <div class="content-wrapper">
      <div class="about-header">
        <h1 class="about-title">About Me</h1>
        <p class="about-description">
          I recently completed my diploma and am currently working as an intern. I have a strong passion for technology and web development, and through my studies and self-learning, I have built a solid foundation in programming and modern web technologies. I am eager to gain practical experience and grow in my professional career.
        </p>
      </div>

      <div class="skills-grid">
        <div class="skill-card">
          <div class="skill-icon web-icon">⟶</div>
          <h3>Web Development</h3>
          <p>Learning to build responsive websites and web apps</p>
        </div>

        <div class="skill-card">
          <div class="skill-icon quick-icon">⛶</div>
          <h3>Quick Learner</h3>
          <p>Adapting fast to new technologies and frameworks</p>
        </div>

        <div class="skill-card">
          <div class="skill-icon self-icon">📖</div>
          <h3>Self-Motivated</h3>
          <p>Continuously learning through courses and projects</p>
        </div>

        <div class="skill-card">
          <div class="skill-icon team-icon">👥</div>
          <h3>Team Player</h3>
          <p>Ready to collaborate and contribute to team success</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script>

<style scoped>
.about-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  min-height: 100vh;
  position: relative;
  overflow: hidden;
}

.about-container::before {
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

.content-wrapper {
  position: relative;
  z-index: 2;
  background: rgba(248, 249, 255, 0.95);
  backdrop-filter: blur(20px);
  border-radius: 12px;
  padding: 1rem;
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
}

.about-header {
  text-align: center;
  margin-bottom: 1rem;
  padding: 0 1rem;
}

.about-title {
  font-size: 3rem;
  font-weight: 800;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa, #c084fc);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 1rem;
}

.about-description {
  font-size: 1.2rem;
  color: #4b5563;
  line-height: 1.7;
  max-width: 1200px;
  margin: 0 auto;
  background: rgba(255, 255, 255, 0.8);
  padding: 1.5rem ;
  border-radius: 16px;
  border: 1px solid rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(10px);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}

.skill-card {
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(15px);
  border-radius: 20px;
  padding: 1.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  border: 1px solid rgba(255, 255, 255, 0.4);
  text-align: center;
  position: relative;
  overflow: hidden;
}

.skill-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, #8b5cf6, #a78bfa);
  z-index: 2;
}

.skill-card:hover {
  transform: translateY(-12px) scale(1.02);
  box-shadow: 0 30px 60px rgba(139, 92, 246, 0.25);
  border-color: rgba(139, 92, 246, 0.3);
}

.skill-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
  display: block;
  filter: drop-shadow(0 4px 8px rgba(0,0,0,0.1));
}

.web-icon {
  color: #8b5cf6;
}

.quick-icon {
  color: #10b981;
}

.self-icon {
  color: #f59e0b;
}

.team-icon {
  color: #ef4444;
}

.skill-card h3 {
  font-size: 1.4rem;
  font-weight: 700;
  color: #1f2937;
  margin-bottom: 1rem;
}

.skill-card p {
  color: #6b7280;
  font-size: 1rem;
  line-height: 1.6;
}

/* Responsive Design */
@media (max-width: 768px) {
  .about-container {
    padding: 1rem;
  }
  
  .content-wrapper {
    padding: 2rem 1.5rem;
    border-radius: 10px;
  }
  
  .about-title {
    font-size: 2.5rem;
  }
  
  .skills-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .skill-card {
    padding: 2rem 1.5rem;
  }
}

@media (max-width: 480px) {
  .about-title {
    font-size: 2.2rem;
  }
  
  .about-description {
    font-size: 1.1rem;
    padding: ;
  }
  
  .skill-card h3 {
    font-size: 1.3rem;
  }
}
</style>