
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
            <h1>Metropolis Series </h1>
          </div>
        </div>

    <div class=" mt-20 h-screen flex flex-col items-center justify-center ml-6 mr-6 mb-6 xl:ml-96 xl:mr-96">

<div class="slider grid grid-cols-1 xl:grid-cols-3 gap-4  rounded-lg  ml-0 mr-0	xl:ml-0 xl:mr-0  xl:translate-y-full  	 image33 ">
        <img class="active h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg  cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-1.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-2.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-3.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-4.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-5.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-6.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-7.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-8.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-9.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-10.jpg" alt="">
        <img class="h-auto max-w-full rounded-lg cursor-pointer hover:scale-105 duration-500" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-11.jpg" alt="">
</div>
<div class="cont-btn">
    <button class="xl:hidden text-4xl btn-nav left text-white"> ← </button>
    <button class="xl:hidden  text-4xl btn-nav right text-white" > →</button>
</div>
</div>
</template>
<style>
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
    @media screen and (max-width: 1200px) {
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