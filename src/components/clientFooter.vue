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

    <h1  class="debug">16+</h1>

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
    white-space: nowrap;
    gap: 5%;
    padding: .8em;
    box-sizing: border-box;
    background-color: white;
    &:hover{background: var(--button-Translucid-Black-Color); color: white; }
      }
#classific{
    width: 55%;
    height: 16vh;
    /* padding: 4% 20%; */
    box-sizing: border-box;
}
menu{
display:flex;
gap: 4em;
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
</style>