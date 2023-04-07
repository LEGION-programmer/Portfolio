<template>
    <div class="content">
        <!-- ToDo List -->
        <div class="content1-item">
            <div class="header header1">
                <h1>ToDo List</h1>
            </div>
            <div class="image">
                <img src="../../assets/projects/todo.jpg" alt="todo">
            </div>
            <div class="description">
                <p>
                    Niemal każdy programista tworzy todo listę. Więc i ja to zrobiłem.
                    Program niby prosty, ale można nauczyć się wielu nowych rzeczy. 
                    Przy tym projekcie chciałem nauczyć się takich technologii jak:
                    Node.js, Express.js, Vue.js, MongoDB. W trakcie tworzenia doszły 
                    jeszcze takie jak: Mongoose, Pinia, Axios, git i GitHub. Dobrze 
                    wspominam ten projekt mimo, że miałem przy nim wiele nerwów z powodu 
                    różnych błędów. Jednak to właśnie te błędy pozwoliły mi się stać lepszym 
                    programistą i nabrać doświadczenia. Nauczyłem się tworzyć schematy kolekcji 
                    z pomocą mongoosa, wykonywać proste akcje na bazie noSQL, tworzyć state i akcje 
                    w pinii, lepiej zrozumiałem działanie vue.js rozdzielania aplikacji na komponenty, 
                    przekazywanie propsów, konfigurowanie ścieżek, wysyłanie żądań HTTP przy pomocy axiosa, 
                    tworzenie REST API itd. Chciałem dodać jeszcze testy jednostkowe, ale spędziłem już 
                    przy tym projekcie tyle czasu, że postanowiłem to odłożyć na przyszłość, a zająć się 
                    tworzeniem nowych projektów.
                </p>
                <a 
                    href="https://github.com/LEGION-programmer/ToDo-List" 
                    target="_blank" 
                    class="read-more-link">
                    Zobacz kod projektu
                </a>
            </div>
        </div>
        <!-- Portfolio/Blog -->
        <div class="content2-item">
            <div class="header header2">
                <h1>Portfolio/Blog</h1>
            </div>
            <div class="image">
                <img src="../../assets/projects/portfolio.jpg" alt="Portfolio/Blog">
            </div>
            <div class="description">
                <p>
                    A oto strona na której się znajdujesz. Tworząc ją chciałem mieć 
                    coś dzięki czemu będę mógł podać więcej informacji na swój temat 
                    i nieco szerzej się o różnych rzeczach rozpisać. Był to też świetny 
                    projekt do poćwiczenia moich umiejętności css, zapoznania się z podstawami scss i 
                    tworzeniu animacji na stronie. Zawsze miałem problem z doborem kolorów, 
                    jednak moja znajoma dała mi kilka porad i myślę, że jest całkiem nieźle. 
                    Bardzo przyjemnie mi się tą stronę tworzyło gdyż nie musiałem budować tutaj 
                    skomplikowanej logiki, więc była to fajna odskocznia po ToDo liście. A samo 
                    stylowanie bardzo mi się spodobało i mam zamiar dalej się w tym rozwijać.
                </p>
                <a 
                    href="https://github.com/LEGION-programmer/Portfolio" 
                    target="_blank" 
                    class="read-more-link">
                    Zobacz kod projektu
                </a>    
            </div>
        </div>
        <!-- Other -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Inne projekty</h1>
            </div>
            <div class="image">
                <img src="../../assets/projects/other.jpg" alt="other">
            </div>
            <div class="description">
                <p>
                    Tworzyłem też wiele innych projektów, ale nigdzie ich nie umieszczałem 
                    kilka z nich dalej jest nieskończonych, a inne tworzyłem na samym początku 
                    mojej nauki programowania i aktualnie trochę wstyd mi je gdziekolwiek 
                    umieszczać (na obrazku aplikacja dla mojej kuzynki do nauki czytania). 
                    Oprócz technologii, o których pisałem wyżej znam jeszcze całkiem dobrze PHP i 
                    jQuery oraz podstawy takich języków jak Python i Java, znam bazę danych mySQL i 
                    potrafię się całkiem dobrze posługiwać językiem SQL. Podczas praktyk w Grecji 
                    tworzyliśmy stronę "Słoneczny Grek", funkcjonalności nie było tam zbyt wiele, ale 
                    udało nam się stworzyć fajny slider i system CMS. Jeśli ktoś się orientuje 
                    jak wyglądają egzaminy zawodowe EE.09/INF.03 to mogę się pochwalić swoim rekordem 
                    wykonania całego egzaminu w około 35min :).
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProjectsContent',

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


}

.read-more-link{
    text-decoration: none;
    font-weight: bolder;
    display: inline-block;
    position: relative;
    width: 50%;
    height: 20px;
    margin-left: 35%;
    background-color: #072AC8;
    color: #FCF300;
    font-size: 15px;
    text-align: center;
    padding: 5px;
    border: 1px solid #FCF300;
    border-radius: 50px;
    box-shadow: 0 5px 1em #000000;
    overflow: hidden;
    transition: all 0.5s;

    &:hover{
        background-position: 150px 0;
        box-shadow: 0 15px 1em #000000;
        cursor: pointer;
    }
}

.read-more-link::after{
    content: ">";
    position: absolute;
    right: 25px;
    opacity: 1;
}

.read-more-link:hover::after{
    animation: animateAfterHover 0.5s forwards;
}

.read-more-link:not(hover)::after{
    animation: animateAfterNotHover 0.5s forwards;
}

.read-more-link::before{ 
    content: ">";
    position: absolute;
    left: -15px;
    opacity: 0;
}

.read-more-link:hover::before{
    animation: animateBeforeHover 0.5s forwards;
}

.read-more-link:not(hover)::before{
    animation: animateBeforeNotHover 0.5s forwards;
}

@keyframes animateAfterHover{
    from{
        right: 25px;
        opacity: 1;
    }
    to{
        right: -10px;
        opacity: 0;
    }
}

@keyframes animateAfterNotHover{
    from{
        right: -10px;
        opacity: 0;
    }
    to{
        right: 25px;
        opacity: 1;
    }
}

@keyframes animateBeforeHover{
    from{
        left: -15px;
        opacity: 0;
    }
    to{
        left: 25px;
        opacity: 1;
    }
}

@keyframes animateBeforeNotHover{
    from{
        left: 25px;
        opacity: 1;
    }
    to{
        left: -15px;
        opacity: 0;
    }
}

@media screen and (max-width: 900px){
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