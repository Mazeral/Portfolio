<template>
  <div class="flex-row">
    <div class="photo">
      <img src="../assets/Welcome_blurry_background _cropped.png" alt="MyPhoto" />
    </div>
    <div class="text">
      <h1>Mohamed Omer Siddig</h1>
      <h4>Software Engineer</h4>
      <img class="icon" src="../assets/icons/programming-svgrepo-com.svg" alt="programming_icon">
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

.icon {
  width: 100px;
  height: 100px;
}

/* استعلامات الوسائط لشاشات الهواتف المحمولة (أقصى عرض 768 بكسل هو الأكثر شيوعًا) */
@media (max-width: 768px) {
  .flex-row {
    flex-direction: column; /* تغيير اتجاه العناصر إلى عمودي */
    align-items: stretch; /* جعل العناصر تمتد على كامل عرض الحاوية */
  }

  .text {
    padding: 1.5rem; /* تقليل الـ padding على الشاشات الصغيرة */
    text-align: center; /* توسيط النص */
  }

  .photo {
    width: 100%; /* جعل الصورة تأخذ كامل عرض الشاشة */
    height: auto; /* الحفاظ على نسبة أبعاد الصورة */
  }
}

/* يمكنك إضافة المزيد من استعلامات الوسائط لأحجام شاشات مختلفة إذا لزم الأمر */
/* مثال لشاشات أصغر */
@media (max-width: 480px) {
  .text h1 {
    font-size: 1.5rem; /* تقليل حجم العنوان */
  }

  .text h4 {
    font-size: 1rem; /* تقليل حجم العنوان الفرعي */
  }

  .icon {
    width: 70px;
    height: 70px;
  }
}
</style>
