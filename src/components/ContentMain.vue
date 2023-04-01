<template>
    <div class="container">
        <div class="content"></div>
    </div>
</template>
<script>
export default {
    name: 'ContentMain'
}
</script>
<style scoped>
.container{
    display: grid;
    grid-template-columns: 130vh;
    justify-content: center;
    align-content: center;
    justify-items: stretch;
    align-items: center;
}

.content{
    display: grid;
    height: 100px;
    grid-template-columns: 1fr 50px;
    justify-content: center;
    align-content: center;
    align-items: center;
    justify-items: stretch;
    background-color: #e8e8e8;
    box-shadow: 0 5px 1em #000000;
    border-radius: 30px;
}
</style>