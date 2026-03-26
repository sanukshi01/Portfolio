<template>
  <section class="featured-projects">
    <!-- Title -->
    <div class="section-header">
      <h1 class="section-title">
        Featured <span class="gradient-text">Projects</span>
      </h1>
      <div class="title-underline"></div>
      <p class="section-subtitle">
        Projects I've built while learning web development. Each project helped me understand core concepts and improve my coding skills.
      </p>
    </div>

    <!-- Projects Grid -->
    <div class="projects-grid">
      <!-- PROJECT 1 – LOCAL IMAGE -->
      <div class="project-card">
        <div class="project-image">
          <img :src="/image1/img.png" alt="Online Pet Shop" />
        </div>
        <div class="project-content">
          <h3 class="project-title">ONLINE PET SHOP</h3>
          <p class="project-desc">
            A user-friendly online pet shop front-end prototype.<br>
            Developed using HTML and CSS.<br>
            Allows users to explore available pets and related products.<br>
            Focuses on clean UI design and basic user interaction
          </p>
        </div>
      </div>

      <!-- PROJECT 2 – placeholder -->
      <div class="project-card">
        <div class="project-image">
          <img src="https://images.unsplash.com/photo-1504639725590-34d0984388bd?w=600&h=400&fit=crop"
               alt="Online Bus Ticket Reservation System" />
        </div>
        <div class="project-content">
          <h3 class="project-title gradient-text">Online Bus Ticket Reservation System</h3>
          <p class="project-desc">
            A responsive and secure web-based ticket booking system.<br>
            Built with HTML, CSS, JavaScript, and PHP.<br>
            Features include multi-user support and secure booking flow.<br>
            Designed with mobile-responsive layout for improved usability.
          </p>
        </div>
      </div>

      <!-- PROJECT 3 – placeholder -->
      <div class="project-card">
        <div class="project-image">
          <img src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=600&h=400&fit=crop"
               alt="QR-Based Self-Ordering System" />
        </div>
        <div class="project-content">
          <h3 class="project-title">QR-Based Self-Ordering System for Restaurants (Ongoing)</h3>
          <p class="project-desc">
            A smart restaurant ordering system using QR code.<br>
            Enables customers to scan QR codes to access the menu and place orders independently.<br>
            Focuses on improving customer experience and reducing wait times.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>


<style scoped>
/* ────── ALL YOUR ORIGINAL STYLES ────── */
.featured-projects {
  min-height: 100vh;
  padding: 6rem 2rem;
  background: linear-gradient(to bottom, #f8fafc 0%, #f1f5f9 100%);
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Header */
.section-header { text-align: center; max-width: 800px; margin-bottom: 4rem; }
.section-title { font-size: 3.5rem; font-weight: 800; color: #1e293b; margin-bottom: .5rem; line-height: 1.1; }
.gradient-text {
  background: linear-gradient(135deg, #8b5cf6 0%, #a78bfa 50%, #c084fc 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.title-underline {
  width: 80px; height: 4px; background: linear-gradient(90deg, #8b5cf6, #a78bfa);
  border-radius: 2px; margin: 1rem auto; box-shadow: 0 0 15px rgba(139,92,246,.4);
}
.section-subtitle { color: #64748b; font-size: 1.1rem; line-height: 1.7; max-width: 600px; margin: 0 auto; }

/* Grid */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 2.5rem;
  max-width: 1200px;
  width: 100%;
}

/* Card */
.project-card {
  background: white; border-radius: 1.5rem; overflow: hidden;
  box-shadow: 0 10px 25px rgba(0,0,0,.08), 0 4px 10px rgba(0,0,0,.05);
  transition: all .4s cubic-bezier(.175,.885,.32,1.275);
  display: flex; flex-direction: column;
}
.project-card:hover {
  transform: translateY(-12px) scale(1.02);
  box-shadow: 0 25px 50px rgba(139,92,246,.2), 0 15px 35px rgba(0,0,0,.12);
}
.project-image { height: 200px; overflow: hidden; position: relative; }
.project-image::after {
  content:''; position:absolute; inset:0;
  background:linear-gradient(transparent 60%,rgba(0,0,0,.1));
}
.project-image img { width:100%; height:100%; object-fit:cover; transition:transform .6s ease; }
.project-card:hover .project-image img { transform:scale(1.1); }
.project-content { padding:1.75rem; flex-grow:1; display:flex; flex-direction:column; }
.project-title { font-size:1.5rem; font-weight:700; color:#1e293b; margin-bottom:.75rem; line-height:1.3; }
.project-desc { color:#64748b; font-size:1rem; line-height:1.6; flex-grow:1; margin-bottom:1rem; }

/* Responsive */
@media (max-width:768px){
  .featured-projects{padding:4rem 1.5rem}
  .section-title{font-size:2.75rem}
  .projects-grid{gap:2rem}
  .project-image{height:180px}
}
@media (max-width:480px){
  .section-title{font-size:2.25rem}
  .project-content{padding:1.5rem}
}
</style>