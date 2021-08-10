<template>
<div class="project">
    <h3 @click="showDetail=!showDetail">{{project.title}}</h3>
  <p v-if="showDetail">{{project.detail}}</p>
</div>
</template>

<script>
export default {
    props:['project'],
    data(){
        return{
            showDetail:false
        }
    }

}
</script>

<style>
.project{
    padding: 20px;
    background-color: #f2f2f2;
    margin: 10px auto;
    cursor: pointer;
}
h3{
    color: indigo;
}

</style>