<template>
<footer class="debug">
    <menu class="debug">
<p id="merchandizer"><span>Não perca nenhum episódio!</span>
<br>Assine nosso podcast em sua plataforma favorita e receba notificações quando<br> lançarmos novos episódios.</p>
<div id="cards" >
<button class="cards"><i class="fa-brands fa-spotify"></i>Spotify   </button>
<button class="cards"><i class="fa-brands fa-apple"></i>Apple Podcasts</button>
<button class="cards"><i class="fa-brands fa-google"></i>Google Podcasts</button>
</div>
    </menu>

<div id="classific" class="debug">

    <div><div><div><h1  class="debug">16+</h1></div></div></div>

</div>
</footer>
</template>

<script setup>





</script>

<style scoped>
footer{
    justify-content: space-between;
    padding: 1.5em;
    box-sizing: border-box;
   display: flex;
}

#merchandizer{text-align: start; }
#cards{
    width: 75%;    
    gap: 10%;
}
.cards{
    font-weight: 500;
    white-space: nowrap;
    gap: 5%;
    padding: .8em;
    box-sizing: border-box;
    background-color: white;
    &:hover{background: var(--button-Translucid-Black-Color); color: white; }
      }
      #classific {
    height: 16vh;
    width: 55%;

    & > div {
        height: 75%;
        width: 75%;
        background-color: aliceblue;

        & > div {
            height: 60%;
            width: 60%;
            background-color: blue;

            & > div {
                height: 50%;
                width: 50%;
                background-color: black;

                & > h1 {
                    font-size: 2em;
                    background: red;
                }
            }
        }
    }
}

          /*text-align: center;
            background-color: purple;
            border-radius: 50%;
            padding: 26% 0%;
            border: 1% solid black; */
        
menu{
display:flex;
gap: 2em;
flex-direction: column;


p{
display: grid;

gap: 10%;

&>span{
    font-size: 200%;
    font-family: Inter;
    font-weight: 700;
 }
    }   
        }
@media (width<=1145px){
    footer{
        width: 80% !important;
        flex-direction: column;
    }
    #cards{
    width: auto;    
    display: grid !important;
    place-items: initial;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr .5fr;
    grid-template-areas: 
    "spot apple"
    "goog ."
    ;
    &:nth-child(1){grid-area:spot ;}
    &:nth-child(2){grid-area:apple ;}
    &:nth-child(3){grid-area:goog ;}
}
.cards{
    font-weight: 500;
    white-space: nowrap;
    gap: 5%;
    padding: .8em;
    background-color: white;
    &:hover{background: var(--button-Translucid-Black-Color); color: white; }
      }
      #classific {
    height: 6vh;
    width: 55%;

    & > div {
        height: 75%;
        width: 75%;
        background-color: aliceblue;

        & > div {
            height: 60%;
            width: 60%;
            background-color: blue;

            & > div {
                height: 50%;
                width: 50%;
                background-color: black;

                & > h1 {
                    font-size: 2em;
                    background: red;
                }
            }
        }
    }
}

          /*text-align: center;
            background-color: purple;
            border-radius: 50%;
            padding: 26% 0%;
            border: 1% solid black; */
        
menu{
display:flex;
gap: 2em;
flex-direction: column;


p{
display: grid;

gap: 5%;

&>span{
    font-size: 200%;
    font-family: Inter;
    font-weight: 400;
 }
    }   
        }
}
</style>