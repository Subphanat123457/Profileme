<template>
    <div class="columns is-gapless is-multiline is-mobile">
        <div class="column">
    <div class="tile is-parent ">
        <div class="tile is-child box border-r">
            <p class="title">{{ messages[language].Title }}</p>
        <div  v-for="(Subtitle, index) in messages[language].Subtitle" :key="index">
          
          <p class="subtitle">{{ messages[language].Subtitle[index] }}</p>
          <p class="subtitle">{{ messages[language].Subtitle2[index] }}</p>
          <p>
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
              <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
            </svg>
            {{ messages[language].p1[index] }}
          </p>
          <p class="magin-b">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
              <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
            </svg>
            {{ messages[language].p2[index] }}
          </p>
        </div>
        </div>
      </div>
    </div>
    <div class="column slider">
        <transition name="fade" tag="div">
            <div>
              <div class="slide" style="padding-left: 20%" v-for="(image, index) in images" :key="index" :class="{ active: index === currentSlide }">
                <img :src="image" alt="" class="slide-image">
              </div>
            </div>
          </transition>
      </div>
    </div>
</template>

<script>
import image1 from '../image/328485517_754050436152164_6737256977798528612_n.jpg';
import image2 from '../image/363793825_760516479202943_4426147079249223690_n.jpg';

export default {
    name: 'Activities',
    props: {
      language: String
    },
    data(){
        return{
            currentSlide: 0,
            images: [image1, image2 
            ],
            messages: {
                en: {
                    Title: 'Activities',
                    Subtitle: ['Comcamp Trainer','Photographer and Video Editor'],
                    Subtitle2: ['Comcamp, Computer Science Camp | Comcamp 21','CSMJU Studio, Maejo University | [Start Date] - Present'],
                    p1: ["Assisted in teaching at Comcamp, focusing on learning about the Internet of Things (IoT).",
                "Capture and edit photographs and videos for CSMJU Studio, contributing to visual content creation."],
                    p2: ["Collaborated with the team to organize a 3-day, 2-night camp to support students in developing IT skills.",
                "Collaborate with the team to ensure high-quality visuals for various projects and events."]
                    
                },
                th: {
                    Title: 'Activities',
                    Subtitle: ['Comcamp Trainer','Photographer and Video Editor'],
                    Subtitle2: ['Comcamp, Computer Science Camp | Comcamp 21','CSMJU Studio, Maejo University | [Start Date] - Present'],
                    p1: ["ช่วยสอนที่ Comcamp โดยเน้นการเรียนรู้เกี่ยวกับ Internet of Things (IoT)",
                "จับภาพถ่ายและแก้ไขวิดีโอสำหรับ CSMJU Studio เพื่อสร้างเนื้อหาที่มีความหลากหลาย"],
                    p2: ["ร่วมมือกับทีมในการจัดค่าย 3 วัน 2 คืน เพื่อสนับสนุนนักศึกษาในการพัฒนาทักษะด้านไอที",
                "ร่วมมือกับทีมในการสร้างภาพที่มีคุณภาพสูงสำหรับโครงการและกิจกรรมต่างๆ"]
                }
            }
        }
    },
    mounted() {
    setInterval(() => {
      this.currentSlide = (this.currentSlide + 1) % this.images.length;
    }, 3000); // Change slide every 3 seconds
  },

}
</script>

<style scoped>
@media (max-width: 600px) {
    .columns {
      flex-direction: column;
    }
  }
.fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
.magin-b{
    margin-bottom: 2rem;
}
.slider {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 50px;
  }
  .slide {
    display: none;
  }
  .slide.active {
    display: block;
  }

  .slide-image {
    width: 50%; /* Set the scale to 50% */
    position: relative;
  }
  

</style>