<template>
    <div class="rating-container">
        <ul>
            <li :class="{active:activeOption==='poor'}"><button @click="activateOption('poor')" type="button">Poor</button></li>
            <li :class="{active:activeOption==='medium'}"><button @click="activateOption('medium')" type="button">Medium</button></li>
            <li :class="{active:activeOption==='great'}"><button @click="activateOption('great')" type="button">Great</button></li>
        </ul>
    </div>
</template>


<script>
export default {
    props:["modelValue"],
    emits:["update:modelValue"],
    data(){
        return{
            activeOption:this.modelValue,
        }
    },
    methods:{
        activateOption(option){
            this.activeOption = option;
            this.$emit("update:modelValue",option);
        }
    },

}
</script>
<style scoped>
.active{
    border:1px solid purple;
}
div.rating-container{
    display: flex;
    flex-direction: row;
}
ul{
    display: flex;
    flex-direction: row;
    list-style: none;
    padding: 0;
    

}
li{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin: 0.2rem;
}
button{
    
    color: black;
    border:none;
    outline: none;
    padding: 0.2rem 1rem;
    cursor:pointer;
    font-weight: bold;

}
button:hover{
    color: rgb(161, 0, 153);
    
}
</style>
