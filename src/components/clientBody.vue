<template>
<main>

    <section id="standard">
        <div class="episode">
            <i class="fa-solid fa-camera"></i>
            <button>{{ epFreq }}</button>
        </div>
        <div class="associedDc">
            <h1>{{ aboutTitle }}</h1>
            <br>
            <span><strong>{{ nameCited }}</strong>
            {{ fistParagraph }}</span>
            <br>
            <span>{{ secnParagraph }}</span>
            <span class="italic"><i>{{ italicPhrase }}</i></span>
        </div>
        


    </section>
    
    <section id="showBefore">
    <h2>Episódios Recentes</h2>
    <a target="_blank" href="{{ linkSeeAll }}">Ver todos</a>
    </section>




    <section id="recently_released">
        <div class="lastestEpisodes">
            <div class="epCount"><button>episódio 1</button>
                 <div class="data">24 Mar 2025</div>
                </div>
            <div class="episodeCounterDc"><h3>Elementos Radioativos da Vida</h3>
                Discutimos os altos e baixos da vida adulta com uma pitada de humor ácido
            </div>
            <div class="itcMin"><p><i class="fa-solid fa-headphones"></i>45 min </p><button><i class="fa-solid fa-play"></i><p>ouvir</p></button></div>

        </div>
        <div class="lastestEpisodes">
            <div class="epCount"><button>episódio 2</button>
                 <div class="data">24 Mar 2025</div>
                </div>
            <div class="episodeCounterDc"><h3>Explosões de Realidade</h3>
                Quando a vida adulta te atinge como uma onda de choque nuclear.
            </div>
            <div class="itcMin"><p><i class="fa-solid fa-headphones"></i> 52 min</p><button><i class="fa-solid fa-play"></i><p>ouvir</p></button></div>

        </div>
        <div class="lastestEpisodes">
            <div class="epCount"><button>episódio 3</button>
                 <div class="data">24 Mar 2025</div>
                </div>
            <div class="episodeCounterDc"><h3>Fórmula Secreta do Caos</h3>
                Ingredientes para sobreviver no mundo moderno sem perder a sanidade.
            </div>
            <div class="itcMin"><p><i class="fa-solid fa-headphones"></i> 38 min</p><button><i class="fa-solid fa-play"></i><p>ouvir</p></button></div>

        </div>

    </section>
   
</main>
</template>

<script setup>
import {ref} from "vue"
const epFreq=ref('NOVO EPISÓDIO TODA SEGUNDA')
const aboutTitle=ref('Sobre o Podcast')
const nameCited=ref('Coquetel de Urânio')

const fistParagraph=ref('é um podcast que mistura o doce da nostalgia com o ácido da realidade adulta.')
const secnParagraph=ref('Como na receita das Meninas Superpoderosas, adicionamos um ingrediente extra à mistura — uma dose de humor ácido e linguagem sem filtro para discutir a vida como ela é.')
const italicPhrase=ref('Açúcar, tempero e tudo que há de bom. Estes foram os ingredientes escolhidos para criar as garotinhas perfeitas. Mas o professor Utônio, acidentalmente, acrescentou um ingrediente extra na mistura — O elemento X!')
const linkSeeAll=ref('https://kzmj4iocb22kqdqbyber.lite.vusercontent.net/')
</script>













<style scoped>
#standard{
height: 60vh;
justify-content: space-between;

}
.episode{
  font-size: 10em;
  color: var(--button-Translucid-Black-Color);
  height: 3.3em;
  border-radius: 12px;
  background:linear-gradient(
    var(--side-Top-Color),
    var(--side-Bottom-Color),
    black 120%
                            ) ;

  &>button{
    background:var(--amarelo-Botão-Mostarda);
    padding: .5em 1em;
    border-radius: 1em;
    font-weight:  600;
    &:hover{
      background: var(--button-Translucid-Black-Color);
      color: var(--Time-Gray-Marker);
    }
  }
}
.associedDc{
  height: 33em;
  background-color: white;
  padding: 8em 2em;
  box-sizing: border-box;
  text-align: start;
  &>h1{
    width: 100%;
  }
  &>span>strong{
    color: var(--roxo-Anchor);
  }
  
}
.italic{
  font-style: italic;
  font-size: small;
  font-weight: 300;
  border: 1px var(--amarelo-Linha-Borda) solid;
  background: var(--amarelo-Fundo-Claro);
}

#showBefore{
  width: 100%;
  justify-content: space-between;
}
#recently_released{
    grid-template-areas:
    "card1 card2 card3",
    "",
    "" ;
    &>:nth-child(1){grid-area:card1 ;}
    &>:nth-child(2){grid-area:card2 ;}
    &>:nth-child(3){grid-area:card3 ;}
    gap: 3%;
}

.lastestEpisodes{

 min-height:12em;
background: linear-gradient(
270deg,
var(--standard-First-Background) 0%,
var(--standard-Second-Background) );

padding-top: 1em;
background-size: 100% 12px;
background-repeat: no-repeat;
background-color: white;
border: gainsboro 2.5px solid;
&:hover{border: var(--hover-Translucid-Violet-Color) 2px solid;
box-shadow: 1px 4px 10px var(--shadow-Card-Box);
}
}
.epCount{
  justify-content: space-between;
  font-weight: 600;
  font-size: .8em;
  padding: 1em 2em .5em 2em;
    box-sizing: border-box;
  &>button{
    cursor:pointer;
    border: var(--hover-Translucid-Violet-Color) 1px solid;
  border-radius: 1em;
  padding: .5% 6px;
  }
  &>.data{
    cursor: pointer;
    color: var(--Time-Gray-Marker);
    font-weight: lighter;
  }
}
.episodeCounterDc{
  text-align: start !important;
  padding: 2em 5%;
  color: var(--Time-Gray-Marker);
  &>h4{
    white-space: nowrap;
    word-break: break-all;
    overflow-wrap: break-word;
    color: black;
  }
}
.itcMin{

  justify-content: space-between;
  &>p{color: var(--Time-Gray-Marker); display: flex; justify-content: space-between; gap:10px;
    padding: 1em 1em 2em 1em;
    box-sizing: border-box;
  }
  &>button{color: var(--roxo-Anchor); background-color: transparent; display: flex; text-align: center; place-items: center ; gap: 6px;
    padding: 1em 2em;
    border-radius: 2em;
    box-sizing: border-box;
    &:hover{
      transition: ease-out 6s !important;
      background:linear-gradient(210deg,transparent,var(--side-Top-Color),transparent) ;
      border: dashed red 1px;
    }
  }

}


@media (width<=1145px) {

  /* Seção do 90% */
  .associedDc,.episode,#showBefore,.lastestEpisodes{
    width: 90% !important;
  }
  section{
      display: flex;
      flex-direction:column ;
      width: fit-content;
      .associedDc{
        width: 50%;
        padding: 2.5%;
      }
    }
    #standard{
      gap: 2em;
    }
    .episode{
    }
    .associedDc{
    }
    #showBefore{
      flex-direction: row;
      justify-content: space-between !important;
      margin:70% 0% 20% 0%;
    }
    #recently_released{
      gap: 1em;
    }
    .lastestEpisodes{
    }
}
</style>
