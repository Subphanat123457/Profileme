<template>
    <div class="columns is-multiline is-mobile">
      <div class="column ">
        <div class="tile is-parent ">
          <div class="tile is-child box border-r">
            <p class="title">{{ messages[language].Title }}</p>
            <p>{{ messages[language].p1 }}</p>
            <p>{{ messages[language].p2 }}</p>
            <p>{{ messages[language].p3 }}</p>
          </div>
        </div>
      </div>
      <div class="column is-one-quarter icon-color">
        <i class="bi bi-facebook"></i>
      </div>
    </div>
  </template>
  
  <script>
  
  export default {
    name: 'Objective',
    props: {
      language: String
    },
    data() {
      return {
        messages: {
          en: {
            Title: 'Objective',
            p1: 'Software Engineering student with strong programming skills and experience in developing web applications. Looking for an internship opportunity to gain hands-on experience in the software development industry.',
            p2: 'A highly motivated and passionate software engineering student with a strong work ethic. Looking for an internship opportunity to contribute to a team and make a difference in the world.',
            p3: 'A self-motivated and team-oriented software engineering student with a strong desire to learn and grow. Looking for an internship opportunity to gain valuable experience and knowledge in the software development industry.',
          },
          th: {
            Title: 'วัตถุประสงค์',
            p1: 'นักศึกษาวิศวกรรมซอฟต์แวร์ที่มีทักษะในการเขียนโปรแกรมและประสบการณ์ในการพัฒนาแอปพลิเคชันเว็บ มองหาโอกาสฝึกงานเพื่อได้รับประสบการณ์ที่จับต้องได้ในอุตสาหกรรมพัฒนาซอฟต์แวร์',
            p2: 'นักศึกษาวิศวกรรมซอฟต์แวร์ที่มีแรงจูงใจและทักษะทางด้านการทำงานที่แข็งแกร่ง มองหาโอกาสฝึกงานเพื่อมีส่วนร่วมในทีมและทำความแตกต่างในโลก',
            p3: 'นักศึกษาวิศวกรรมซอฟต์แวร์ที่มีความกระตือรือร้นและเป็นทีม มีความตั้งใจที่จะเรียนรู้และเติบโต มองหาโอกาสฝึกงานเพื่อได้รับประสบการณ์และความรู้มีค่าในอุตสาหกรรมพัฒนาซอฟต์แวร์',
          },
        },
      };
    },
    watch: {
      language() {
        console.log('Language changed to:', this.language);
      }
    }
  };
  </script>
  
  <style scoped>
  .text-color {
    color: #000000;
  }
  .border-r{
    border-right: 1px ridge #0f0f0f;
  }
  .icon-color{
    color: #0f0f0f;
  }
  </style>
  