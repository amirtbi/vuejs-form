<template>
    <div class="rating-container">
        <p id="rating-description">Rate your experience</p>
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
    background-color: blueviolet;
    color: white;
}
div.rating-container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    padding: 1.2rem;
}
ul{
    display: flex;
    flex-direction: row;
    list-style: none;
    padding: 0;
    margin: 0;
    

}
li{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin: 0.2rem;
}
p#rating-description{
    font-weight: bold;
    font-family: inherit;
    text-transform: uppercase;
}
button{
    
    color: white;
    border:none;
    outline: none;
    padding: 0.4rem 1rem;
    cursor:pointer;
    
    font-family: "Karla", sans-serif;
    background-color: var(--secondaryBubbleColor);
    border-radius: 2px;

}
button:hover{
    color: white;
    background-color: var(--primaryColor);
    
}
</style>
