<template>
  <div>
    
    <div class="h-screen md:overflow-hidden  ">
      <div class="mt-10 text-white hauteur 		">
        <div class="flex flex-col justify-center text-center items-center overflow-hidden text-6xl  ">
          <div class="titre mr-6 ml-6  text-5xl">
            <h1>New Collection </h1>
            <h1>Metropolis Series </h1>
          </div>
        </div>
        <div class="hauteur   md:flex   p-12 justify-center gap-x-4  md:overflow-hidden	">
          <div class="hover:scale-95	 duration-500">

          <img src="../assets/1.jpeg" alt="" class="hover:shadow-blue-100/30 hover:shadow-2xl		 duration-500 translate-y-full object-cover  	image1	">
          </div>

          <br>
          <div class="hover:scale-95	 duration-500">
          <img src="../assets/2.jpeg" alt="" class="hover:shadow-blue-100/30  hover:shadow-2xl	 duration-500 translate-y-full 	object-cover image2	">
          </div>

          <br>
          <div class="hover:scale-95 duration-500">
          <img src="../assets/3.jpeg" alt="" class="	 duration-500 hover:shadow-blue-100/30 hover:shadow-2xl	  translate-y-full object-cover 	image3	">
          </div>
          <div class="md:hidden h-20 bg-black">

    </div>
        </div>
      </div>
      
    </div>
    
    <div class=" fixed bottom-6 left-1/2 transform   -translate-x-2/4">
      <div class="bg-black bouton rounded-xl outline-1 outline-white	outline-double		 shadow w-44 text-2xl text-center">
        
        <button class=" text-white hover:text-neutral-500 ">
          <a class=" " href="/collection">Voir Collection</a>
        </button>
      </div>
    </div>
  </div>
</template>
<script>


</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
.hauteur{
  height: 90vh;
}

.titre{
  transform: translateY(-100%);

  animation: slidein2 2s forwards;
  animation-delay: 1300ms;

}
.bouton{
  opacity:  0;
  transform: translateY(100%);
  animation: slidein3 2s forwards 2000ms, floating 3s infinite 400ms;

}

@keyframes floating {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-5px); }
}

.image1 {
  @media screen and (max-width: 1200px) {
    height: 20rem;
    width: 20rem;
  }
  height:40rem ;
  width: 30rem;
  
  animation: slidein 3s forwards;
}


.image2 {
  @media screen and (max-width: 1200px) {
    height: 20rem;
    width: 20rem;
  }
    
  height:40rem ;
  width: 30rem;
  
  animation: slidein 3s forwards;
  animation-delay: 100ms;

}

.image3 {
  @media screen and (max-width: 1200px) {
    height: 20rem;
    width: 20rem;
  }
  height:40rem ;
  width: 30rem;
  
  animation: slidein 3s forwards;
  animation-delay: 200ms;
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
@keyframes slidein3 {
  from {
    opacity: 0;
    transform: translateY(200%);
  }

  to {
    opacity: 1;
    transform: translateY(0%);
  }
}
@keyframes slidein2 {
  from {
    opacity: 0;
    transform: translateY(-200%);
  }

  to {
    opacity: 1;
    transform: translateY(0%);
  }
}
@keyframes slidein3 {
  from {
    opacity: 0;
    transform: translateY(100%);
  }

  to {
    opacity: 1;
    transform: translateY(0%);
  }
}


html {
  scroll-behavior: smooth;
} 

.h{

  box-shadow: 0 2px 2px 1px rgba(128, 127, 127, 0.2);

}
.teest{
  font-family: 'VT323', monospace;

}

.v-enter-active,
.v-leave-active {
  transition: all 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
  transform: translateY(-100%);
}
</style>