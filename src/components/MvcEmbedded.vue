<script>
export default {
    data () {
    return {
      url: null
    }
  },
  async mounted () {

    this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/List/?embedded=true` // Список заявок новый абитуриент
    //this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/ListForConfinder/?embedded=true` // Список заявок новый абитуриент (конфайдер)
    //this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/?embedded=true` // Заявка новый абитуриент
    //this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/{eventGuid}?embedded=true` // Заявка новый абитуриент (редактирование)
    //this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/CreateEventForConfinder/?embedded=true` // Заявка новый абитуриент (конфайдер)
    //this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/editEventForConfinder/?embedded=true` // Заявка новый абитуриент (конфайдер) редактирование
    //this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/List/?embedded=true` // Заявка новый абитуриент (ДПО)
    //this.url = `https://optest.roweb.online/workspace.2/student/Enrollment/List/?embedded=true` // Список заявок новый абитуриент (ДПО)
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