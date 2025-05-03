<template>
  <div class="contact-section">
    <h1 class="contact-title">Contact Me:</h1>
    <h4 class="contact-subtitle">If You Want From Us To Work Together, You Can Contact Me Using The Email:</h4>
    <h5 class="contact-email">mohamedsiddig5026485@gmail.com</h5>
	<h4>Or:</h4>
    <div class="contact-methods">
      <a href="https://www.linkedin.com/in/mohamed-omer-siddig-ahmed-05172b231/" 
         target="_blank" 
         rel="noopener noreferrer" 
         class="contact-link">
        <i class="fab fa-linkedin"></i> LinkedIn
      </a>
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;1,300&display=swap");
* {
  font-family: Montserrat;
}

.contact-section {
  display: flex;
  flex-direction: column;
  align-items: center; /* This centers child elements horizontally */
  gap: 1.5rem;
  padding: 2rem;
  max-width: 800px;
  margin: 0 auto;
  text-align: center; /* Ensures text inside centered containers stays centered */
}

.contact-title {
  font-size: 2.5rem;
  font-weight: 500;
  margin-bottom: 0.5rem;
}

.contact-subtitle {
  font-weight: 300;
  font-size: 1.25rem;
  max-width: 600px;
  line-height: 1.6;
}

.contact-email {
  font-size: 1.1rem;
  font-weight: 400;
  margin-bottom: 1rem;
}

.contact-methods {
  display: flex;
  justify-content: center;
  width: 100%;
}

.contact-link {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  background: rgba(0, 0, 0, 0.05);
  border-radius: 8px;
  text-decoration: none;
  color: #2c3e50;
  font-size: 1.2rem;
  transition: all 0.3s ease;
}

/* Rest of your existing styles... */
</style>
