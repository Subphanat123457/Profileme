<template>
    <div class="column margin-t">
        <div class="tile is-parent ">
          <div class="tile is-child box border-r">
            <p class="title">{{ messages[language].Title }}</p>
            <p>
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot" viewBox="0 0 16 16">
                <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3"/>
              </svg>
              {{ messages[language].p1 }}
            </p>
          </div>
        </div>
      </div>
</template>

<script>
export default {
    name: 'Certificate',
    props: {
      language: String
    },
    data() {
      return {
        messages: {
          en: {
            Title: 'Certificate',
            p1: 'Supanat Wiboonpanit received a certificate in the Basic Cyber Security Training program from NET Managed Services co., ltd. with a score of 80%. This demonstrates that Supannat Wiboonpanit has strong skills and knowledge in Basic Cyber Security Training. These skills and knowledge will allow Supannat Wiboonpanit to be effective in the Security role.',
          },
          th: {
            Title: 'Certificate',
            p1: 'ศุภณัฐ วิบูลย์พานิช ได้รับ Certificate ในหลักสูตร Basic Cyber Security Training จาก NET Managed Services co., ltd. ด้วยคะแนน 80% ซึ่งแสดงให้เห็นว่า ศุภณัฐ วิบูลย์พานิช มีทักษะและความรู้ใน Basic Cyber Security Training เป็นอย่างดี ทักษะและความรู้เหล่านี้จะช่วยให้ ศุภณัฐ วิบูลย์พานิช สามารถปฏิบัติงานในตำแหน่ง Security ได้อย่างมีประสิทธิภาพ',
          }
        }
      }
    },

    methods: {
      toggleLanguage() {
        this.$emit('updateLanguage', this.language === 'en' ? 'th' : 'en');
      }
    }

}
</script>

<style scoped>
.margin-t{
    margin-top: -2rem;
}

</style>>
