<template>
  
<header>
        <button>16+</button>

        <div class="starTitle">
            <h1>{{ title }}</h1>
        <img :src="sparkleIcon" alt="Sparkle" />
        </div>
        <p>{{subTitle}}</p>

            <nav>

            <button>
                <i class="fa-solid fa-play"></i><p>Ouvir Agora</p>
            </button>
            <!-- /////////////////////////////////////// -->
            <button>
                <i class="fa-solid fa-rss"></i><p>Assinar</p>
            </button>
            </nav>
            <details><summary>
              <i class="fa-brands fa-github"></i></summary>
              <a href="https://github.com/Thales-N-O" target="_blank" >Meu git</a>
            </details>
            <details>
              <summary>
                <i class="fa-brands fa-linkedin"></i>
              </summary>
              <a href="https://www.linkedin.com/in/thales-nascimento-oliveira"
               target="_blank" >Meu linkedin</a>
            </details>

</header>

</template>

<script setup>
import sparkleIcon from '@/assets/sparkle.svg';
import {ref} from "vue"

const title=ref("Coquetel de Urânio")

const subTitle=ref('Açúcar, tempero e tudo que há de bom... mais um ingrediente extra na mistura!')

</script>



<style scoped>
header{


  /* //COSTUMIZAÇÃO DO LAYOUT GRID AREA SE MEXER PODE DAR MERDA// */
  grid-template-columns: .5fr 1fr .5fr; /* 3 colunas */
  grid-template-rows: .2vh 10vh 10vh .2vw ; /* 4 linhas */
  grid-template-areas: 
  ". clage ."
  ". title github"
  ". paragraph ."
  ". play linkedin"
  ;
  /* /////////////////////////////////////////////////// */
    &>:nth-child(1){grid-area:clage ;}
    &>:nth-child(2){grid-area:title ;}
    &>:nth-child(3){grid-area:paragraph;}
    &>:nth-child(4){grid-area:play ; }
    &>:nth-child(5){grid-area:github ;} 
    &>:nth-child(6){grid-area:linkedin ; }
      /* CONFIGURAÇÔES DO BUTTON QUE NECESSITAVA DE UM ARQUIVO CSS */
    &>button:nth-of-type(1){
      border-radius: 1em;
      padding:.3em 1em;
      box-sizing: content-box;
      color: white;
      border: white solid 1px;
      background-color: transparent;
      &:hover{
        background-color: hotpink;
        box-shadow: 5px 6px 1px crimson;
      }
                          }
    &>nav>button:nth-of-type(1){
      color:white;
      border: solid 1px var(--button-Green-Color);
      background: var(--button-Green-Color);
      padding: .8em 2em .8em 2em;
        gap: 1em;
      &:hover{
        border: none;
        background-color:var(--button-Light-Green-Color-Hover);
      }
                          }
    &>nav>button:nth-of-type(2){
      color:white;
      border: solid 1px white;
      background: white;
      padding: .8em 2em .8em 2em;
        gap: 1em;
      &:hover{
        background-color: var(--button-Translucid-White-Color);
        color: black;
      }
      
}
&>.starTitle{
    text-align: center;
    font-family: var(--fonte-Titulo);
    font-size: 1.8vw;
    white-space: nowrap;
    font-style: bold;
    
  }
  &>p{
    font-size: larger;
    font-weight:500;
  }
}
img{
    position: relative;
    bottom: .75em;
    right:.5em;
height: 70%;
filter:  invert(1) sepia(1.5) saturate(20);
}
nav{
    gap: 2em;
    display: flex;
    justify-content: space-between;
}


















@media (max-width:560px) {
  header{
    width: 90%	;
    /* //COSTUMIZAÇÃO DO LAYOUT GRID AREA SE MEXER PODE DAR MERDA// */
  grid-template-columns: 1fr 1fr 1fr; /* 3 colunas */
  grid-template-rows: 1fr 1fr 1fr 1fr; /* 4linhas */
  grid-template-areas: 
  ". clage ."
  ". title ."
  ". play github "
  ". paragraph linkedin"
  
  ;
    &>:nth-child(1){grid-area:clage ;}
    &>:nth-child(2){grid-area:title ; font-size: small;}
    &>:nth-child(3){grid-area:paragraph;}
    &>:nth-child(4){grid-area:play;}
    &>:nth-child(5){grid-area:github ;}
    &>:nth-child(6){grid-area:linkedin;}
  /* /////////////////////////////////////////////////// */
  }
  
  details{
  background: none;
  border: none;
  text-align: center;
  box-sizing: border-box;
  padding: 0vh 1.5vw;
  text-wrap: nowrap;
  &>summary{
    font-size: 10vw;
  }
  &[open]{
    border: none;
  }
  }

}

</style>