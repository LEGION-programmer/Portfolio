<template>
    <div class="content">
        <!-- Experience -->
        <div class="content1-item">
            <div class="header header1">
                <h1></h1>
            </div>
            <div class="image">
                
            </div>
            <div class="description">
                <p></p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'AboutContent',
}
</script>
<style lang="scss" scoped>
*{
    font-family: sans-serif;
}

.content{
    display: grid;
    height: auto;
    background-color: #e8e8e8;
    box-shadow: 0 5px 1em #000000;
    border-radius: 30px;
}

.content1-item{
    display: grid;
    grid-template-columns: 70vh 60vh;
    grid-template-areas: 
    "header ."
    "image description"
    ; 
    justify-content: center;
}

.content2-item{
    display: grid;
    grid-template-columns: 60vh 70vh;
    grid-template-areas: 
    ". header"
    "description image"
    ; 
    justify-content: center;
}

.header{
    grid-area: header;

    &.header1{
        justify-self: end;
    }

    &.header2{
        justify-self: start;
    }

    >h1{
        color: #072AC8;
        font-size: 30px;
        margin: 20px;
    }
}

.image{
    grid-area: image;
    justify-self: center;
    align-self: center;

    >img{
        width: 90%;
        height: 300px;
        border: 1px solid #FCF300;
        border-radius: 200px;
        box-shadow: 0 5px 1em #000000;
        margin: 20px;
    }
}

.description{
    grid-area: description;
    justify-self: center;
    align-self: center;


    >p{
        color: #3B322C;
        font-size: 18px;
        text-align: center;
        margin: 10px;
    }

    >button{
        transition: 0.5s;
        width: 30%;
        height: 40px;
        margin: 10px;
        margin-left: 35%;
        background-color: #072AC8;
        color: #FCF300;
        border: 1px solid #FCF300;
        border-radius: 50px;
        box-shadow: 0 5px 1em #000000;
        overflow: hidden;
    }

    >button:hover{
        transition: 0.5s;
        background-position: 150px 0;
        box-shadow: 0 15px 1em #000000;
        cursor: pointer;
    }
}
</style>