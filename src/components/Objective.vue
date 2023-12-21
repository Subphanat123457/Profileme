<template>
    <div class="columns is-multiline is-mobile is-full">
      <div class="column ">
        <div class="tile is-parent ">
          <div class="tile is-child box border-r">
            <p class="title">{{ messages[language].Title }}</p>
            <p>
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
                <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
              </svg>
              {{ messages[language].p1 }}
            </p>
            <p>
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
                <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
              </svg>
              {{ messages[language].p2 }}
            </p>
            <p>
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
                <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
              </svg>
              {{ messages[language].p3 }}
            </p>
            <p>
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
                <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
              </svg>
              {{ messages[language].p4 }}
            </p>
          </div>
        </div>
      </div>
      <div class="column is-one-quarter-desktop is-full-mobile icon-color">
        <contract />
      </div>
    </div>
  </template>
  
  <script>
import Contract from './contract.vue';

  export default {
  components: { Contract },
    name: 'Objective',
    props: {
      language: String
    },
    data() {
      return {
        messages: {
          en: {
            Title: 'Caeer Objective',
            p1: 'I intend to attend the internship to develop my skills and build a side project as a basis for personal development and promote a deeper understanding of the overall picture of software development.',
            p2: 'The ability to communicate clearly is my hallmark of being ready to share my knowledge and technical experience. Both in Thai and English.',
            p3: 'I strive to manage my time efficiently to create good results and punctuality on project deadlines.',
            p4: 'I am a developer who is passionate about working with teams and has the ability to solve problems effectively as a team.',
          },
          th: {
            Title: 'Caeer Objective',
            p1: 'ฉันตั้งใจที่จะเข้าร่วมการฝึกงานเพื่อพัฒนาทักษะของฉันและสร้างโครงการด้านข้างเพื่อเป็นพื้นฐานสําหรับการพัฒนาส่วนบุคคลและส่งเสริมความเข้าใจที่ลึกซึ้งยิ่งขึ้นเกี่ยวกับภาพรวมของการพัฒนาซอฟต์แวร์',
            p2: 'ความสามารถในการสื่อสารที่ชัดเจนเป็นจุดเด่นของฉันที่พร้อมที่จะแบ่งปันความรู้และประสบการณ์ทางเทคนิค ทั้งในภาษาไทยและภาษาอังกฤษ',
            p3: 'ฉันมุ่งมั่นที่จะจัดการเวลาของฉันอย่างมีประสิทธิภาพเพื่อสร้างผลงานที่ดีและตรงต่อเวลาตามกำหนดโปรเจค',
            p4: 'ฉันคือนักพัฒนาที่หลงไหลในการทำงานร่วมกับทีมและมีความสามารถในการแก้ไขปัญหาแบบทีมอย่างมีประสิทธิภาพ'
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
  