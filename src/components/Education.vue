<template>
    <div class="tile is-parent ">
        <div class="tile is-child box border-r">
          <p class="title">{{ messages[language].Title }}</p>
          <p class="subtitle">{{ messages[language].Subtitle }}</p>
          <p class="subtitle">{{ messages[language].Subtitle2 }}</p>
          <p>
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
              <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
            </svg>
            {{ messages[language].p1 }}
          </p>
        </div>
      </div>
</template>

<script>
export default {
    name: 'Education',
    props: {
      language: String
    },
    data(){
        return{
            messages: {
                en: {
                    Title: 'Education',
                    Subtitle: 'Undergraduate Studies (Ongoing)',
                    Subtitle2: 'Maejo University, Year Level 3 - Expected Graduation [Month/Year]',
                    p1: "Currently pursuing my bachelor's degree at Maejo University in Computer Since. The diverse curriculum and academic support from experienced faculty members have equipped me with the knowledge and skills essential for a professional software developer.",
                },
                th: {
                    Title: 'Education',
                    p1: 'ฉันกำลังศึกษาอยู่ที่คณะเทคโนโลยีสารสนเทศ สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง สาขาวิชาเทคโนโลยีสารสนเทศ ฉันกำลังศึกษาอยู่ในชั้นปีที่ 3',
                }
            }
        }
    }

}
</script>

<style>

</style>