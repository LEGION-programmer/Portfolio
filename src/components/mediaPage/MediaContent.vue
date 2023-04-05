<template>
    <div class="content">
        <!-- Discord -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Discord</h1>
            </div>
            <div class="image">
                <img src="../../assets/about/photo3.jpg" alt="code">
            </div>
            <div class="description">
                <p>
                    Nie sądziłem, że aż tak mi się to spodoba. A jednak!
                    Jeszcze w pierwszej klasie technikum uważałem, że programowanie
                    jest nudne. Dopiero na początku 3 klasy rozbudziła się we mnie
                    chęć do programowania i uczenia się nowych technologii.
                    Najpierw chciałem stworzyć prostą aplikacje w pythonie dla
                    mojej małej kuzynki, która pomogła by jej w nauce czytania.
                    Szybko zauważyłem, że JavaScript będzie do tego lepszy choć 
                    uważałem go za bardzo dziwny język i nic nie umiałem. Po pół roku
                    aplikacja była gotowa i posłużyła mi do nauki nowych rzeczy.
                    Teraz tworze coraz więcej, gdyż mam do tego coraz większe chęci 
                    i mimo że mój GitHub nie jest jeszcze zbyt obszerny to stworzyłem
                    już wiele projektów i będzie ich coraz więcej.
                </p>
            </div>
        </div>
        <!-- Gym -->
        <div class="content2-item">
            <div class="header header2">
                <h1>Sporty siłowe</h1>
            </div>
            <div class="image">
                <img src="../../assets/about/photo1.jpg" alt="gym">
            </div>
            <div class="description">
                <p>
                    Siłownia interesuje mnie już od wielu lat. Mimo, że nie mam 
                    wspaniałej formy to zawsze chętnie się na nią wybieram lub 
                    ćwiczę w domu. Chyba nie ma lepszego uczucia niż spompowane 
                    mięśnie po ciężkim treningu. Wiele osób też nienawidzi mieć 
                    zakwasów, a ja lubię, ponieważ wiem, że wykonałem solidny trening. 
                    Kolejnym plusem zakwasów jest, to że czuć mięsień przy każdym jego 
                    spięciu przez co mam wrażenie, że jest większy i rośnie mi ego :). 
                    Natomiast kiedy brakuje mi motywacji, a wiem że mam wystarczająco siły 
                    i czasu na trening lubie obejrzeć jakiś film motywacyjny np. z Ronniem Colmanem
                    lub stare występy Facelessa w strength wars.
                </p>    
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