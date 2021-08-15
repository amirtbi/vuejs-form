<template>
    <header>
        <h1 class="header-title">Contact Us</h1>
        <p>Any questions or remarks, Just write us a message !</p>
    </header>
</template>


<style scoped>
    header{
        display: flex;
        flex-direction: column;
        width:100vw;
        background:var(--primaryColor);
        justify-content: center;
        align-items: center;
        
    }

    h1,p{
        padding: 1rem;
        margin:0;
        color:white;
        font-family: inherit;
    }
    p{
        filter: opacity(0.5);
        padding:0px 0px 10px 0;

    }
</style>