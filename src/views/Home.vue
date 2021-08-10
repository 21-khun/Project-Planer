<template>
<h1>Home</h1>
<div v-for="project in projects" :key="project.id">

  <SingleProject :project="project"></SingleProject>

</div>
</template>

<script>



import SingleProject from '../components/SingleProject'
export default {
  name: 'Home',
  data(){
    return{
      projects:[]
    }
  }
  ,
  components: {
    SingleProject,
   

  },
  mounted(){
    fetch('http://localhost:3000/projects')
    .then((response)=>{
     return response.json()

    })
    .then((datas)=>{
      this.projects=datas
      

    })
    .catch(()=>{

    })
  }
}
</script>
