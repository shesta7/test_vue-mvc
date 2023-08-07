<script>
export default {
    data () {
    return {
      res: null
    }
  },
  async mounted () {
    const response = await fetch('https://optest.roweb.online/workspace.2/student/Enrollment/List',  {
        credentials: "include"
      });
      let html = await response.text();
      let parser = new DOMParser();
	    let doc = parser.parseFromString(html, 'text/html');
      
      let links = doc.querySelectorAll("link")
      links.forEach(x=> document.head.append(x))
      
      let scripts = doc.querySelectorAll("script")
      scripts.forEach((script) => {
        
        let newScript = document.createElement("script");
        newScript.src = script.src.replace('local.roweb.online:31000', 'optest.roweb.online');
        script.parentNode.removeChild(script);
        newScript.addEventListener("load", event => script);
        newScript.addEventListener("error", event => script);
        document.body.appendChild(newScript);
  });

//scripts.forEach(x=> document.body.append(x))
      

      let page = doc.querySelector('#global-loader').innerHTML + 
      doc.querySelector('main').innerHTML
      
      this.res = page
      
      
      //document.getElementById('superDiv_').innerHTML = page
  },
}
</script>

<template>
  <iframe src="https://optest.roweb.online/workspace.2/student/Enrollment/List/" style="position:fixed; top:0; left:0; bottom:0; right:0; width:100%; height:100%; border:none; margin:0; padding:0; overflow:hidden; z-index:999999;"></iframe>
    <div id="superDiv_" v-html="res"></div>
	
</template>