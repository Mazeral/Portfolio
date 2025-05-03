<template>
  <div class="experience-container">
    <h1 class="title">My Experience:</h1>
    <h4 class="certificate-text">I Have A Training Certificate On Software Engineering From ALX</h4>
    <div class="certificate-image">
      <img src="../assets/17-short-specializations-certificate-mohamed-ahmed.png" alt="ALX Certificate">
    </div>
    <h4 class="projects-title">And I Made Multiple Side Projects, Here's Some Of Them:</h4>
    <ul class="projects-list">
      <li><a href="https://github.com/Mazeral/ChitChat" target="_blank" rel="noopener noreferrer">ChitChat</a></li>
      <li><a href="https://github.com/Mazeral/Algorithm-Visualizer" target="_blank" rel="noopener noreferrer">Algorithm-Visualizer</a></li>
      <li><a href="https://github.com/Mazeral/HealthVault" target="_blank" rel="noopener noreferrer">HealthVault</a></li>
    </ul>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;1,300&display=swap");

.experience-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  font-family: 'Montserrat';
  padding: 2rem;
}

.title {
  text-align: center;
  margin-bottom: 1rem;
}

.certificate-text {
  text-align: center;
  margin: 1rem 0;
}

.certificate-image {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 1rem 0;
  padding: 1rem;
  background: #f5f5f5;
  border-radius: 8px;
}

.certificate-image img {
  max-width: 100%;
  max-height: 300px;
  object-fit: contain;
}

.projects-title {
  text-align: center;
  margin: 2rem 0 1rem 0;
}

.projects-list {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  padding: 0;
  margin: 0 auto;
  max-width: 600px;
  list-style: none;
}

.projects-list li {
  padding: 0.8rem 1.5rem;
  background: rgba(0, 0, 0, 0.05);
  border-radius: 6px;
  width: 100%;
  text-align: center;
  transition: all 0.3s ease;
}

.projects-list li:hover {
  background: rgba(0, 0, 0, 0.1);
  transform: translateY(-2px);
}

a, a:link, a:visited{
  text-decoration: none;
  color: black;
}
/* Responsive adjustments */
@media (max-width: 768px) {
  .title {
    font-size: 2rem;
  }
  .certificate-text, .projects-title {
    font-size: 1.2rem;
  }
  .projects-list li {
    padding: 0.6rem 1rem;
  }
}
</style>
