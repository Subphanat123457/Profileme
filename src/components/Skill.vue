<template>
    <div class="columns">
        <div class="column">
            <div class="tile is-parent ">
                <div class="tile is-child box border-r">
                  <p class="title">{{ messages[language].Title1 }}</p>
                  <div v-for="(Skill1, index) in messages[language].Skill1" :key="index" >
                    <p>
                        {{ Skill1 }}
                        <progress class="progress is-info" :value="messages[language].ScoreSkill1[index]" max="100">45%</progress>
                    </p>
                </div>
                </div>
              </div>
        </div>
        <div class="column">
            <div class="tile is-parent ">
                <div class="tile is-child box border-r">
                  <p class="title">{{ messages[language].Title2 }}</p>
                  <div v-for="(Skill2, index) in messages[language].Skill2" :key="index" >
                    <p>
                        {{ Skill2 }}
                        <progress class="progress is-info" :value="messages[language].ScoreSkill2[index]" max="100">45%</progress>
                    </p>
                </div>
                </div>
              </div>
        </div>
        <div class="column">
            <div class="tile is-parent ">
                <div class="tile is-child box border-r">
                  <p class="title">{{ messages[language].Title3 }}</p>
                    <div v-for="(Skill3, index) in messages[language].Skill3" :key="index" >
                        <p>
                            {{ Skill3 }}
                            <progress class="progress is-info" :value="messages[language].ScoreSkill3[index]" max="100">45%</progress>
                        </p>
                    </div>
                </div>
              </div>
        </div>
        <div class="column">
            <div class="tile is-parent ">
                <div class="tile is-child box border-r">
                  <p class="title">{{ messages[language].Title4 }}</p>
                  <div v-for="(Skill4, index) in messages[language].Skill4" :key="index" >
                    <p>
                        {{ Skill4 }}
                        <progress class="progress is-info" :value="messages[language].ScoreSkill4[index]" max="100">45%</progress>
                    </p>
                </div>
                </div>
              </div>
        </div>
      </div>
  
</template>

<script>
export default {
    name: 'Skill',
    props: {
      language: String
    },
    data(){
        return{
            messages: {
                en: {
                    Title1: 'Programing Language',
                    Title2: 'Database',
                    Title3: 'Framework',
                    Title4: 'Tools',
                    Skill1: [ 'Java', 'Python','C++', 'C', 'HTML', 'JavaScript', 'CSS'],
                    Skill2: ['MySQL'],
                    Skill3: ['Vue.js', 'Bootstrap' , 'react.js'],
                    Skill4: ['Git', 'GitHub', 'Visual Studio Code', 'Microsoft Office', 'Unity'],
                    ScoreSkill1: [60, 70, 30, 65, 70, 50, 50],
                    ScoreSkill2: [65],
                    ScoreSkill3: [70, 70, 30],
                    ScoreSkill4: [75, 70, 90, 75, 45],
                },
                th: {
                    Title1: 'ภาษาโปรแกรม',
                    Title2: 'ฐานข้อมูล',
                    Title3: 'เฟรมเวิร์ค',
                    Title4: 'เครื่องมือ',
                    Skill1: [ 'Java', 'Python','C++', 'C', 'HTML', 'JavaScript', 'CSS'],
                    Skill2: ['MySQL'],
                    Skill3: ['Vue.js', 'Bootstrap' , 'react.js'],
                    Skill4: ['Git', 'GitHub', 'Visual Studio Code', 'Microsoft Office', 'Unity'],
                    ScoreSkill1: [60, 70, 30, 65, 70, 50, 50],
                    ScoreSkill2: [65],
                    ScoreSkill3: [70, 70, 30],
                    ScoreSkill4: [75, 70, 90, 75, 45],
                }
              }
        }
    }

}
</script>

<style>

</style>