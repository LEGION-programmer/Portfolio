<template>
    <div class="content">
        <!-- ZPUE -->
        <div class="content1-item">
            <div class="header header1">
                <h1>ZPUE S.A.</h1>
            </div>
            <div class="image">
                <img src="../../assets/experience/photo1.jpg" alt="zpue">
            </div>
            <div class="description">
                <p>
                    W czerwcu 2022 roku rozpocząłem miesięczne praktyki w firmie ZPUE S.A.
                    w dziale help desk. Podczas praktyk realizowałem swoje obowiązki takie jak: 
                    wydawanie sprzętu komputerowego do innych działów, przygotowywanie sprzętu 
                    komputerowego dla nowych pracowników, montaż stanowisk pracy, klonowanie 
                    dysków maszyn produkcyjnych, rozwiązywanie problemów zgłaszanych przez innych 
                    pracowników, naprawianie sprzętu komputerowego i sieciowego. Podczas tych praktyk 
                    miałem możliwość zobaczyć jak działają duże firmy, poznać nowe programy wykorzystywane 
                    przez nie oraz rozwinąć umiejętność współpracy z nowo poznanymi ludźmi.
                </p>
            </div>
        </div>
        <!-- Intershiep Greec -->
        <div class="content2-item">
            <div class="header header2">
                <h1>Praktyki w Grecji</h1>
            </div>
            <div class="image">
                <img src="../../assets/experience/photo5.jpg" alt="robot">
            </div>
            <div class="description">
                <p>
                    Pod koniec września 2022 roku wyjechałem na zagraniczne praktyki 
                    do Grecji organizowane przez Zespół Szkól Nr 2 im. Hetmana Stefana 
                    Czarnieckiego we Włoszczowie, współfinansowanego przez Unię Europejską. 
                    Praktyki odbyły się w Olympus Education Services Single Member P.C.. 
                    Podczas praktyk ćwiczyliśmy swoje umiejętność w wykonywaniu następujących zadań: 
                    Przygotowywanie do pracy zgodnie z zasadami BHP; Montowanie i eksploatowanie sprzętu 
                    komputerowego oraz instalowanie i zarządzanie jego oprogramowaniem; Konfigurowanie i 
                    administrowanie sieciowymi systemami operacyjnymi; Tworzenie, zarządzanie, modyfikowanie i 
                    wykorzystywane funkcjonalności baz danych; Tworzenie, programowanie i zarządzanie aplikacjami 
                    internetowymi; Oprócz tego zajmowaliśmy się składaniem i programowaniem robotów, mieliśmy 
                    możliwość rozwijania swoich umiejętność pracy w grupie oraz składaliśmy drukarkę 3D, do której 
                    później przygotowywaliśmy projekty do wydruku. Dzięki temu, że praktyki odbyły się za 
                    granicą mieliśmy możliwość poprawić swój język angielski i poznać grecką kulturę, gdyż w 
                    dni wolne od praktyk zwiedzaliśmy takie miejsca jak Ateny, Tesaloniki, wyspę Skiatos i wiele innych miejsc.
                    Po zakończeniu praktyk dostaliśmy certyfikaty oraz Europassa.
                </p>    
            </div>
        </div>
        <!-- INF.02 -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Kwalifikacja zawodowa INF.02</h1>
            </div>
            <div class="image">
                <img src="../../assets/experience/photo6.jpg" alt="inf.02">
            </div>
            <div class="description">
                <p>
                    31 sierpnia 2022 roku zdobyłem certyfikat kwalifikacji zawodowej INF.02.
                    Zakres kwalifikacji obejmuje: Administrację i eksploatację systemów komputerowych, 
                    urządzeń peryferyjnych i lokalnych sieci komputerowych.
                </p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'ExperienceContent',

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