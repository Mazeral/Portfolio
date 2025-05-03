<template>
  <div class="flex-row">
    <div class="text">
      <h1>Mohamed Omer Siddig</h1>
      <h4>Software Engineer</h4>
	  <img class="icon" src="../assets/icons/programming-svgrepo-com.svg" alt="programming_icon">
    </div>
    <div class="photo">
      <img src="../assets/Welcome_blurry_background _cropped.png" alt="MyPhoto" />
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;1,300&display=swap");

.flex-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--color-background);
}
.text {
  padding: 3rem;
  font-family: Montserrat;
}
.photo {
  height: 600px;
  width: 38.2%;
  overflow: hidden;
}
.icon{
	width:100px;
	height:100px;
}
</style>
