<script lang="ts">
    let { slideGalapagos } = $props();
    let slideIndex = $state(1);

    function showSlide(n:number) {
        slideIndex = n;
        if (slideIndex > slideGalapagos.length) slideIndex = 1;
        if (slideIndex < 1) slideIndex = slideGalapagos.length;
    }

    function plusSlide(n:number) {
        showSlide(slideIndex + n);
    }

    function currentSlide(n:number) {
        showSlide(n);
    }

</script>

<article class="shadow-md">
  <div class="slideshow-container relative mx-auto max-w-screen-lg">
      {#each slideGalapagos as slide, index (slide.src)}
          <div class="my-slides fade" class:hidden={index + 1 !== slideIndex}>
              <div class="number absolute bg-(--info) m-3 right-0 p-2 rounded-full text-white font-medium">{index + 1} / {slideGalapagos.length}</div>
              <img src={slide.src} alt="Picture {index + 1}" class="w-full" />
              <div class="text-white absolute bottom-0 left-0 text-center w-full p-2 bg-(--info) text-lg">{index+1}. {slide.caption}</div>
          </div>
      {/each}
  
      <button onclick={() => plusSlide(-1)} aria-label="chevron-left" class="absolute top-1/2 cursor-pointer left-0 transform -translate-y-1/2"><i class='bx bxs-chevron-left text-5xl text-white'></i></button>
      <button onclick={() => plusSlide(1)} aria-label="chevron-right" class="absolute top-1/2 right-0 transform -translate-y-1/2 cursor-pointer"><i class='bx bxs-chevron-right text-5xl text-white'></i></button>
  
  </div>
  <div class="dots text-center mt-2">
      {#each slideGalapagos as slide, i}
          <button onclick={() => currentSlide(i + 1)} aria-label="dot" class="dot bg-(--info) inline-block w-4 h-4 rounded-full mx-1 cursor-pointer" class:bg-(--info-hover)={i + 1 === slideIndex}></button>
      {/each}
  </div>
</article>

<style>
  .fade {
    animation: fade 1.5s;
  }

  @keyframes fade {
    from {
      opacity: 0.4;
    }
    to {
      opacity: 1;
    }
  }
</style>