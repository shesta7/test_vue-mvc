<script>
export default {
    data () {
    return {
      url: null
    }
  },
  async mounted () {

    this.url = `https://optest.roweb.online/workspace.2/admission/enrollment/search/?embedded=true` // Список заявок новый абитуриент
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment/?embedded=true` // Заявка новый абитуриент
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment/{eventGuid}?embedded=true` // Заявка новый абитуриент (редактирование)
      
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment-confider/search/?embedded=true` // Список заявок новый абитуриент (конфайдер) 
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment-confider/?embedded=true` // Заявка новый абитуриент (конфайдер)
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment-confider/{eventGuid}?embedded=true` // Заявка новый абитуриент (конфайдер) редактирование
    
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment-dpo/search/?embedded=true` // Список заявок новый абитуриент (ДПО)  
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment-dpo/?embedded=true` // Заявка новый абитуриент (ДПО)
    //this.url = `https://optest.roweb.online/workspace.2/admission/enrollment-dpo/{eventGuid}?embedded=true` // Заявка новый абитуриент (ДПО) (редактирование)
  },
}
</script>

<template>
  <iframe :src="url"></iframe>	
</template>

<style scoped>
iframe {
  position:fixed; 
  top:0; 
  left:0; 
  bottom:0; 
  right:0; 
  width:100%; 
  height:100%; 
  border:none; 
  margin:0; 
  padding:0; 
  overflow:hidden; 
  z-index:999999;
}
</style>
