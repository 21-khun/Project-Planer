<template>
<div class="project">
    <div class="flexBox">
        <div>
            <h3 @click="showDetail=!showDetail">{{project.title}}</h3>
            <p v-if="showDetail">{{project.detail}}</p>

        </div>
        <div>
            <span class="material-icons">
                delete
            </span>
            <span class="material-icons">
                edit
            </span>
            <span class="material-icons">
                done
            </span>

        </div>
    </div>
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
    border-left: 10px solid crimson;
    border-radius: 10px ;
}
h3{
    color: indigo;
    cursor: pointer;

}
.flexBox{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
span{
    margin-left: 10px;
    cursor: pointer;

}
    span:hover{
        color: blue;
    }

</style>