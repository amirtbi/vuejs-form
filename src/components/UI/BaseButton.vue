<template>

    <button :class="mode" :mode="mode">
        <slot></slot>
    </button>

</template>
<script>
export default {
    props:["mode"]
}
</script>

<style scoped>
.action{
    color:white;
    font-family: "Karla", sans-serif;
    padding: 1rem 2rem;
    font-weight: bold;
    background-color: var(--primaryColor);
    border: none;
    border-radius: 3px;
    outline: none;
    cursor: pointer;
    transition: ease-in-out 0.5s;

}
.action:hover{
    background-color: var(--accentColor);
    color:black;
}
div.button-container{
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-content: center;
    width: 100%;
    margin-top: 1rem;
    padding: 1.2rem;
}
</style>