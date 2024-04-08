<template>
    <div class="content">
        <!-- Discord -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Discord</h1>
            </div>
            <div class="image">
                <img src="../../assets/media/photo3.jpg" alt="discord">
            </div>
            <div class="description">
                <p>
                    Tutaj jestem najbardziej aktywny, więc tutaj też będę najszybciej 
                    odpisywał. Można dołączyć do mojego 
                    <a href="https://discord.gg/RMbJxusqMG" target="_blank">serwera</a> 
                    i tam się ze mną kontaktować
                    lub pisać do mnie w wiadomości prywatnej: Legion#2513.
                </p>
            </div>
        </div>
        <!-- YouTube -->
        <div class="content2-item">
            <div class="header header2">
                <h1>YouTube</h1>
            </div>
            <div class="image">
                <img src="../../assets/media/photo1.jpg" alt="youtube">
            </div>
            <div class="description">
                <p>
                    Filmów mam mało i rzadko coś dodaje, gdyż robię to głównie 
                    dla siebie. Gdy mam pomysł na jakiś nowy materiał to siadam 
                    i go przygotowuję. Są to głównie materiały z gier z podłożoną 
                    muzyką i fajnie pocięte akcje. Mój kanał możesz znaleźć
                     <a href="https://www.youtube.com/channel/UC82F6crRTKfV3WeoC54oxlQ" target="_blank">tutaj</a>.
                </p>    
            </div>
        </div>
        <!-- Twitch -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Twitch</h1>
            </div>
            <div class="image">
                <img src="../../assets/media/photo2.jpg" alt="twitch">
            </div>
            <div class="description">
                <p>
                    Podobnie jak w przypadku youtuba streamy robię rzadko, gdyż 
                    z nieznanych mi przyczyn mimo, że podczas streamowania lub nagrywania
                    mam stałe fps (przynajmniej 60), a na nagraniu/streamie wygląda jakbym 
                    miał 20-30fps. Nie mniej jednak staram się to poprawić, a jeśli masz ochotę 
                    mnie śledzić, możesz mnie znaleźć <a href="https://www.twitch.tv/legion_tenprawdziwy" target="_blank">tutaj</a>.
                </p>
            </div>
        </div>
         <!-- Instagram -->
         <div class="content2-item">
            <div class="header header2">
                <h1>Instagram</h1>
            </div>
            <div class="image">
                <img src="../../assets/media/photo4.jpg" alt="instagram">
            </div>
            <div class="description">
                <p>
                    Instagrama założyłem niedawno, więc aktualnie zbyt wiele tam nie ma, 
                    ale z biegiem czasu będę dodawał nowe zdjęcia więc myślę, że warto mnie 
                    obserwować <a href="https://www.instagram.com/_l.3.g.1.o.n_/" target="_blank">tutaj</a>.
                </p>    
            </div>
        </div>
        <!-- GitHub -->
        <div class="content1-item">
            <div class="header header1">
                <h1>GitHub</h1>
            </div>
            <div class="image">
                <img src="../../assets/media/photo5.jpg" alt="GitHub">
            </div>
            <div class="description">
                <p>
                    Projektów obecnie może i mało, ale szybko ich przybywa. Moje repozytoria 
                    zawsze są publiczne dla osób, które byłyby zaciekawione śledzeniem moich postępów. 
                    Wszelkie uwagi lub pytania możecie zadawać na moim serwerze discord, a mojego 
                    GitHuba możecie zobaczyć <a href="https://github.com/LEGION-programmer?tab=repositories" target="_blank">tutaj</a>.
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
    width: 100%;
    display: grid;
    height: auto;
    background-color: #e8e8e8;
    box-shadow: 0 5px 1em #000000;
    border-radius: 30px;
}

.content1-item{
    display: grid;
    width: 100%;
    grid-template-columns: 1fr 1fr;
    grid-template-areas: 
    "header ."
    "image description"
    ; 
    justify-content: center;
}

.content2-item{
    display: grid;
    grid-template-columns: 1fr 1fr;
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
        width: 80%;
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
}

@media screen and (max-width: 600px){
    .content1-item{
        grid-template-areas: 
        "header header"
        "image image"
        "description description"
        ; 

    }

.content2-item{
        grid-template-areas: 
        "header header"
        "image image"
        "description description"
        ; 

    }
}
</style>