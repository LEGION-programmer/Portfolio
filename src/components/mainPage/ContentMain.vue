<template>
    <div class="content">
        <!-- Experience -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Doświadczenie</h1>
            </div>
            <div class="image">
                <img src="../../assets/home/experience.jpg" alt="experience">
            </div>
            <div class="description">
                <p>
                    Aktualnie jestem uczniem 4 klasy szkoły średniej na kierunku 
                    technik informatyk. Zdobyłem certyfikat kwalifikacji INF.02 
                    (Administracja i eksploatacja systemów komputerowych, urządzeń 
                    peryferyjnych i lokalnych sieci komputerowych). Odbyłem miesięczne 
                    praktyki w firmie ZPUE S.A. w dziale help desk oraz miesięczne 
                    praktyki w Grecji Olympus Education Services Single Member P.C. 
                    w ramach projektu "Wkrocz w przyszłość".
                </p>

                <h2 class="read-more-link" @click="experience()">Czytaj dalej</h2>
            </div>
        </div>
        <!-- Projects -->
        <div class="content2-item">
            <div class="header header2">
                <h1>Projekty i technologie</h1>
            </div>
            <div class="image">
                <img src="../../assets/home/projects.jpg" alt="projects">
            </div>
            <div class="description">
                <p>
                    Aktualnie znam takie technologie jak: JavaScript, HTML, CSS, Vue,
                    Node.js, Express.js, MongoDB, Mongoose, React.js, TypeSrcipt na poziomie dobrym. Oprócz 
                    tego znam PHP na poziomie średnim oraz podstawy Java oraz Python. 
                    Znam podstawowe zasady tworzenia stron RWD, założenia OOP oraz podstawy
                    pracy z gitem i gitHubem.
                </p>

                <h2 class="read-more-link" @click="projects()">Czytaj dalej</h2>
            </div>
        </div>
        <!-- About -->
        <div class="content1-item">
            <div class="header header1">
                <h1>O mnie</h1>
            </div>
            <div class="image">
                <img src="../../assets/home/experience.jpg" alt="about">
            </div>
            <div class="description">
                <p>
                    Jestem Tomek mam 20 lat i szkole się na full stack web 
                    developera. Lubię uprawiać sport zwłaszcza chodzić na siłownię 
                    oraz jeździć na rowerze, w upalne dni chętnie jeżdżę motocyklem.
                    Lubię spotykać się ze znajomymi, a po ciężkim dniu chętnie 
                    siedzę z przyjaciółmi na discordzie i razem z nimi w coś gram.
                </p>

                
                <h2 class="read-more-link" @click="about()">Czytaj dalej</h2>
            </div>
        </div>
        <!-- Media -->
        <div class="content2-item">
            <div class="header header2">
                <h1>Media</h1>
            </div>
            <div class="image">
                <img src="../../assets/home/media.jpg" alt="media">
            </div>
            <div class="description">
                <p>
                    Posiadam podstawowe media społecznościowe takie jak facebook i
                    snapchat, choć najbardziej aktywny jestem zdecydowanie na 
                    discordzie. Posiadam swojego gitHuba, twitcha gdzie raz na jakiś 
                    czas zrobię streama oraz kanał na YouTube gdzie czasami wrzucę 
                    jakiś fajnie zmontowany film. Jeśli jesteś zainteresowany odwiedzeniem
                    niektórych moich mediów kliknij przycisk poniżej.
                </p>

                <h2 class="read-more-link" @click="media()">Czytaj dalej</h2>
            </div>
        </div>
        <!-- Contact -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Kontakt</h1>
            </div>
            <div class="image">
                <img src="../../assets/home/contact.png" alt="contact">
            </div>
            <div class="description">
                <p>
                    Kontaktować można się ze mną najlepiej za pomocą discorda, gdyż
                    jak już wspomniałem tam jestem najbardziej aktywny, facebooka gdzie
                    również powinienem szybko odpowiedzieć oraz mailem tam zaglądam najrzadziej.
                </p>

                <h2 class="read-more-link" @click="contact()">Czytaj dalej</h2>     
            </div>
        </div>
    </div>
</template>
<script>
import { useRouter } from 'vue-router'

export default {
    name: 'ContentMain',

    data() {
    return {
      router: useRouter()
    }
  },
    methods: {
        about(){
        this.router.push({ name: 'about' })
        },

        home(){
        this.router.push({ name: 'home' })
        },

        experience(){
        this.router.push({ name: 'experience' })
        },

        projects(){
        this.router.push({ name: 'projects' })
        },

        media(){
        this.router.push({ name: 'media' })
        },

        contact(){
        this.router.push({ name: 'contact' })
        }
    }
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
    width: 100%;
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
    display: inline-block;
    position: relative;
    width: 40%;
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
    right: 15px;
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