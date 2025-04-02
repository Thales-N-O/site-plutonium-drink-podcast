<template>
<footer>
<p id="merchandizer"><span>Não perca nenhum episódio!</span>
<br>Assine nosso podcast em sua plataforma favorita e receba notificações quando lançarmos novos episódios.</p>
<div id="cards">
<button class="cards">Spotify   </button>
<button class="cards">Apple Podcasts</button>
<button class="cards">Google Podcasts</button>
</div>

<div id="classific"><h1 >16+</h1></div>
</footer>
</template>

<script setup>
</script>

<style scoped>
footer{
    justify-content: space-between;
    grid-template-columns: 60% 20%;
    grid-template-rows: repeat(2, auto);
    padding: 2em;
    box-sizing: border-box;
    grid-template-areas: 
    "merchandizer classific"
    "cards classific"
    ;
}

#merchandizer{text-align: start;  grid-area: merchandizer;}
#cards{
    grid-area:cards;
    display: flex;
    gap: 10em;
}
.cards{
    padding: .8em;
    box-sizing: border-box;
    background-color: white;
    &:hover{background: var(--button-Translucid-Black-Color); color: white; }
      }
#classific{grid-area: classific;}
</style>