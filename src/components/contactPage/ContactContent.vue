<template>
    <div class="content">
        <!-- Discord -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Discord</h1>
            </div>
            <div class="image">
                <img src="../../assets/contact/photo1.jpg" alt="discord">
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
        <!-- Facebook -->
        <div class="content2-item">
            <div class="header header2">
                <h1>Facebook/Messenger</h1>
            </div>
            <div class="image">
                <img src="../../assets/contact/photo3.jpg" alt="facebook/messenger">
            </div>
            <div class="description">
                <p>
                    Tutaj również jestem całkiem aktywny więc szybko będę odpisywał.
                    Nie trzeba mnie dodawać do znajomych wystarczy wysłać mi prywatną wiadomość.
                    <a href="https://www.facebook.com/tomek.kaczmarek.79" target="_blank">Facebook/Messenger</a>
                </p>    
            </div>
        </div>
        <!-- Gmail -->
        <div class="content1-item">
            <div class="header header1">
                <h1>Gmail</h1>
            </div>
            <div class="image">
                <img src="../../assets/contact/photo4.jpg" alt="Gmail">
            </div>
            <div class="description">
                <p>
                    Na maila wchodzę najrzadziej, ale zawsze odpisuję, więc 
                    jeśli nie dostałeś jeszcze odpowiedzi spokojnie, na pewno 
                    w końcu odpiszę: tomaszlegionkaczmarek@wp.pl 
                    <a href="mailto:tomaszlegionkaczmarek@wp.pl">Napisz do mnie</a>
                </p>
            </div>
        </div>
        <!-- Phone -->
        <div class="content2-item">
            <div class="header header2">
                <h1>Numer telefonu</h1>
            </div>
            <div class="image">
                <img src="../../assets/contact/photo5.jpg" alt="phone">
            </div>
            <div class="description">
                <p>
                    Numer telefonu podaję dopiero po rozpoczęciu współpracy, 
                    w celu szybszej komunikacji i uniknięciu ciągłego wydzwaniania obcych ludzi.
                </p>    
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'ContactContent',

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