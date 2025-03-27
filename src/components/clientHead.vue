<template>
  
<header>
        <button>16+</button>
        <div class="starTitle">
            <h1>Coquetel de Urânio</h1>
        <img :src="sparkleIcon" alt="Sparkle" />
        </div>
        <p>Açúcar, tempero e tudo que há de bom... mais um ingrediente extra na mistura!</p>
            <nav>
            <button>Ouvir Agora</button>
            <button>Assinar</button>
            </nav>
</header>

</template>

<script setup>
import sparkleIcon from '@/assets/sparkle.svg';
</script>
<style scoped>
header{
    &>:nth-child(1){grid-area:clage ;}
    &>:nth-child(2){grid-area:title ;}
    &>:nth-child(3){grid-area:paragraph;}
    &>:nth-child(4){grid-area:play ;}
    &>:nth-child(5){grid-area:singup ;}





    &>button:nth-of-type(1){
        border-radius: 10em;
        width:5em;
        color: white;
        border: white solid 1px;
        background: transparent;
        &>::after{
            content: " ";
  display: inline-block;
  width: 10px;
  height: 10px;
  background: red;
  border-radius: 50%;
  margin-right: 5px;
  box-shadow: 
    15px 0px 0px blue,  /* Segundo ponto (azul) */
    30px 0px 0px yellow; /* Terceiro ponto (amarelo) */;
        }
                            }
    &>button:nth-of-type(2){
        color:chocolate;
                            }
    &>button:nth-of-type(3){
        color: violet;
                            }
    
}
img{
height: 70%;
filter:  invert(1) sepia(1.5) saturate(20);
}

</style>