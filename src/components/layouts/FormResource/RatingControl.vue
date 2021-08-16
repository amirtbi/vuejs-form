<template>
    <div class="rating-container">
        <ul>
            <li><button>Poor</button></li>
            <li><button>Medium</button></li>
            <li><button>Great</button></li>
        </ul>
    </div>
</template>


<script>
export default {
    
}
</script>
<style scoped>
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
    background-color: var(--accentColor);
    color: purple;
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
