
<template>
    <ul class="fixed w-screen block mt-10 flex test justify-between  max-h-24  text-white z-40 text text-lg top-0 right-4  xl:right-0 item-center drop-shadown-xl p-7">
    <li>
      <NuxtLink to="/">

        <button class=" bg-neutral-900 xl:bg-black p-2 shadow-2xl flex    rounded-xl xl:ml-4 ">
          <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6 "
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
          >
          <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M15 19l-7-7 7-7"
          />
          </svg>
          <h2 class="hidden sm:block teest text-xl xl:text-xl">
            Retour a l'accueil
          </h2>
        </button>
      </NuxtLink>
    
        </li>
   
  </ul>

 <div class="flex flex-col justify-center mt-10 text-center items-center overflow-hidden text-6xl  ">
          <div class="titre2 mr-6 ml-6   text-white text-4xl xl:text-5xl">
            <h1>Collection </h1>
            <h1>Desert Series </h1>
          </div>
        </div>

    <div class=" mt-20 h-screen  ml-6 mr-6 mb-6 xl:ml-96 xl:mr-96">

<div class="slider xl:grid  xl:grid-cols-3 gap-4 flex  justify-center  rounded-lg  ml-0 mr-0	xl:ml-0 xl:mr-0  xl:translate-y-full  	 image33 ">
        <img class="active h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500 collection" src="../assets/1.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/2.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/3.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/4.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/5.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/6.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/7.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/8.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/9.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/10.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/11.png" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500 collection" src="../assets/12.png" alt="">
</div>
<div class="cont-btn image33">
    <button class="xl:hidden text-4xl btn-nav left text-white"> ← </button>
    <button class="xl:hidden  text-4xl btn-nav right text-white" > →</button>
</div>
<footer class="bg-neutral-900 rounded-lg m-4  ">
        <div class="w-screen-xl items-center p-4 flex flex-col md:flex-row md:justify-between">
            <span class="text-md text-white sm:text-center ">© 2023 
                <a class="">Projet Collection Hugo, Tous droits réservés</a>
        
            </span>
            <ul class="flex flex-wrap items-center mt-3 text-sm font-medium text-white mr-0 gap-4 md:mr-16 sm:mt-0">
                <li>
                    <a href="https://www.linkedin.com/in/hugo-rytlewski-b06841281/">
                    <img  class="w-6" src="~/assets/linkdinwhite.png" alt="">  
                    </a>  
                </li>
                <li>
                    <a href="https://github.com/HugoRytlewski">
                      <img  class="w-6" src="~/assets/githubwhite.png" alt="">    
                    </a>
                </li>
                
            </ul>
        </div>
    </footer>
    <br>
  </div>



</template>

<style>
.collection{
  height: 17rem;
  width: 23rem;
  object-fit: cover;
  object-position: center ;
    
}
.image33{
  
@media screen and (min-width: 1200px) {

    animation: slidein 1s forwards;
  animation-delay: 200ms;
}
}

@keyframes slidein {
  from {
    opacity: 0;
    transform: translateY(200%);
  }

  to {
    opacity: 1;
    transform: translateY(0%);
  }
}
.titre2{
  transform: translateY(100%);

  animation: slidein2 1s forwards;
  animation-delay: 300ms;


}
.slider{
    overflow: hidden;

}
.slider img{
    @media screen and (max-width: 1280px) {
        display: none;
        
        
  }


}
img.active{
    display: block;
    animation: fade 0.5s ;

}
@keyframes fade{
    from{
        transform: translateX(-350px);
    }
    to{
        transform: translateX(0px);
    }
}
.cont-btn{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 2rem;
    gap: 1rem;
}
</style>
<script>
export default {
  mounted() {
    const items = document.querySelectorAll('img');
    const nbSlide = items.length;
    const suivant = document.querySelector('.right');
    const precedent = document.querySelector('.left');
    let count = 0;

    function slideSuivante(){
        items[count].classList.remove('active');

        if(count < nbSlide - 1){
            count++;
        } else {
            count = 0;
        }

        items[count].classList.add('active');
        console.log(count);
    }
    suivant.addEventListener('click', slideSuivante);

    function slidePrecedente(){
        items[count].classList.remove('active');

        if(count > 0){
            count--;
        } else {
            count = nbSlide - 1;
        }

        items[count].classList.add('active');
        console.log(count);
    }

    precedent.addEventListener('click', slidePrecedente);
  }
}
</script>