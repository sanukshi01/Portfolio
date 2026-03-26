<template>
  <section class="education">
    <div class="container">
      <!-- Background Decorations -->
      <div class="bg-decor">
        <div class="decor-1"></div>
        <div class="decor-2"></div>
        <div class="decor-3"></div>
      </div>

      <div class="content">
        <div class="section-header">
          <h1 class="section-title">
            <span class="title-icon">🎓</span>
            Education
          </h1>
          <div class="title-underline"></div>
        </div>

        <div class="timeline">
          <!-- ATI Card -->
          <div class="timeline-item current">
            <div class="timeline-dot present-dot"></div>
            <div class="edu-card">
              <div class="card-header">
                <div class="card-icon">🏛️</div>
                <h2>ADVANCED TECHNOLOGICAL INSTITUTE</h2>
                <div class="card-badge present-badge">Present</div>
              </div>
              <div class="card-body">
                <p class="degree">Higher National Diploma in Information Technology</p>
                <div class="timeline-bar"></div>
                <div class="date">2023 - Present</div>
              </div>
            </div>
          </div>

          <!-- A/L Card -->
          <div class="timeline-item">
            <div class="timeline-dot completed-dot"></div>
            <div class="edu-card">
              <div class="card-header">
                <div class="card-icon">📚</div>
                <h2>T/SRI SHANMUGA HINDU LADIES' COLLEGE</h2>
                <div class="card-badge completed-badge">2021</div>
              </div>
              <div class="card-body">
                <p class="degree">A/L – B in Carnatic Music, C in Geography, C in Tamil</p>
                <p class="成绩">Z-Score: 0.6148</p>
                <div class="timeline-bar"></div>
                <div class="date">Completed 2021</div>
              </div>
            </div>
          </div>
        </div>

        <!-- Stats -->
        <div class="stats-grid">
          <div class="stat-card">
            <div class="stat-number">2+</div>
            <span>Years of Study</span>
          </div>
          <div class="stat-card">
            <div class="stat-number">1</div>
            <span>Diploma Program</span>
          </div>
          <div class="stat-card">
            <div class="stat-number">3</div>
            <span>A/L Subjects</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Education",
};
</script>

<style scoped>
.education {
  min-height: 100vh;
  background: linear-gradient(135deg, #0f0f23 0%, #1a0f2e 50%, #2a1a4d 100%);
  position: relative;
  overflow: hidden;
  padding: 4rem 2rem;
  display: flex;
  align-items: center;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

.container {
  max-width: 1000px;
  margin: 0 auto;
  position: relative;
}

/* Background Decorations */
.bg-decor {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  pointer-events: none;
  z-index: 1;
}

.decor-1, .decor-2, .decor-3 {
  position: absolute;
  border-radius: 50%;
  background: linear-gradient(45deg, transparent, rgba(139, 92, 246, 0.1));
}

.decor-1 {
  width: 200px;
  height: 200px;
  top: 10%;
  left: 10%;
  animation: float 8s ease-in-out infinite;
}

.decor-2 {
  width: 150px;
  height: 150px;
  bottom: 20%;
  right: 15%;
  animation: float 10s ease-in-out infinite reverse;
}

.decor-3 {
  width: 100px;
  height: 100px;
  top: 60%;
  left: 5%;
  animation: float 12s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0) scale(1); }
  50% { transform: translateY(-20px) scale(1.05); }
}

/* Section Header */
.section-header {
  text-align: center;
  margin-bottom: 4rem;
  position: relative;
  z-index: 2;
}

.section-title {
  font-size: 3rem;
  font-weight: 900;
  background: linear-gradient(135deg, #ffffff, #e5e7eb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}

.title-icon {
  font-size: 3.5rem;
  animation: bounce 2s ease-in-out infinite;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

.title-underline {
  width: 100px;
  height: 4px;
  background: linear-gradient(90deg, #8b5cf6, #a78bfa);
  margin: 1rem auto 0;
  border-radius: 2px;
  animation: expand 1s ease-out;
}

@keyframes expand {
  from { width: 0; }
  to { width: 100px; }
}

/* Timeline */
.timeline {
  position: relative;
  margin-bottom: 4rem;
  z-index: 2;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 4px;
  background: linear-gradient(to bottom, #8b5cf6, #a78bfa);
  transform: translateX(-50%);
  border-radius: 2px;
  box-shadow: 0 0 20px rgba(139, 92, 246, 0.3);
}

.timeline-item {
  position: relative;
  margin-bottom: 3rem;
  display: flex;
  align-items: center;
}

.timeline-item.current {
  flex-direction: row-reverse;
}

.timeline-item:not(.current) {
  flex-direction: row;
}

.timeline-dot {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  z-index: 3;
  box-shadow: 0 0 20px rgba(139, 92, 246, 0.5);
}

.present-dot {
  background: linear-gradient(135deg, #10b981, #34d399);
}

.completed-dot {
  background: linear-gradient(135deg, #f59e0b, #fbbf24);
}

/* Education Cards */
.edu-card {
  flex: 1;
  max-width: 450px;
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 20px;
  padding: 2rem;
  margin: 0 2rem;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
}

.edu-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, #8b5cf6, #a78bfa);
}

.edu-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 25px 50px rgba(139, 92, 246, 0.2);
  border-color: rgba(139, 92, 246, 0.3);
}

.card-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.card-icon {
  font-size: 2rem;
  width: 60px;
  height: 60px;
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
  color: white;
  flex-shrink: 0;
}

.card-header h2 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #ffffff;
  margin: 0;
  flex: 1;
}

.card-badge {
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  color: white;
}

.present-badge {
  background: linear-gradient(135deg, #10b981, #34d399);
}

.completed-badge {
  background: linear-gradient(135deg, #f59e0b, #fbbf24);
}

.card-body {
  position: relative;
}

.degree {
  font-size: 1.1rem;
  color: #e5e7eb;
  margin: 0 0 0.5rem 0;
  font-weight: 500;
}

成绩 {
  color: #a78bfa;
  font-weight: 600;
  margin: 0 0 1rem 0;
}

.timeline-bar {
  height: 2px;
  background: linear-gradient(90deg, transparent, #8b5cf6, transparent);
  margin: 1rem 0;
}

.date {
  color: #9ca3af;
  font-size: 0.95rem;
  font-weight: 500;
}

/* Stats Grid */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 2rem;
  margin-top: 3rem;
  z-index: 2;
}

.stat-card {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 16px;
  padding: 2rem 1.5rem;
  text-align: center;
  transition: all 0.3s ease;
  cursor: pointer;
}

.stat-card:hover {
  transform: translateY(-5px);
  border-color: #8b5cf6;
  box-shadow: 0 15px 30px rgba(139, 92, 246, 0.2);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 900;
  background: linear-gradient(135deg, #8b5cf6, #a78bfa);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  display: block;
  margin-bottom: 0.5rem;
}

.stat-card span {
  color: #d1d5db;
  font-size: 0.95rem;
  font-weight: 500;
}

/* Responsive Design */
@media (max-width: 768px) {
  .education {
    padding: 2rem 1rem;
  }
  
  .section-title {
    font-size: 2.5rem;
  }
  
  .title-icon {
    font-size: 3rem;
  }
  
  .timeline::before {
    left: 30px;
  }
  
  .timeline-item {
    flex-direction: column !important;
    margin-left: 60px;
  }
  
  .timeline-dot {
    left: 20px;
  }
  
  .edu-card {
    margin: 0 !important;
    max-width: none;
  }
  
  .stats-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .section-title {
    font-size: 2rem;
  }
  
  .card-header {
    flex-direction: column;
    text-align: center;
    gap: 0.5rem;
  }
  
  .card-icon {
    width: 50px;
    height: 50px;
    font-size: 1.5rem;
  }
}
</style>