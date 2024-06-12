<template>
  <div class="slider-wrapper">
    <div class="wrapper">
      <span id="before" class="btn">Natura <br />Clear </span>

      <div class="gallery">
        <div class="gallery__resize">
          <img
            src="~/assets/img/b1.png"
            alt=""
            class="img img-before blend-mode-luminosity"
          />
        </div>
        <div id="myDIV">
          <img src="~/assets/img/b1.png" alt="" class="img img-after" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const gallery = document.querySelector('.gallery')
  const galleryResize = document.querySelector('.gallery__resize')
  const before = document.querySelector('#before')
  const after = document.querySelector('#after')

  gallery.addEventListener('mousemove', (event) => {
    let x = event.offsetX
    galleryResize.style.width = x + 'px'
    galleryResize.classList.remove('tr')
  })

  // Diğer fonksiyonları da buraya taşıyabilirsiniz.
})
</script>

<style scoped>
#myDIV {
  background: white;
}
#myDIV img {
  mix-blend-mode: luminosity;
}
.slider-wrapper {
  width: 100%;
  padding: 0;
  margin: 0;
  display: flex;
  flex: 1;
  justify-content: center;
  align-items: center;
}
.wrapper,
.gallery,
.img {
  height: auto;
  margin: 0;
  padding: 0;
}
.wrapper {
  position: relative;
}
.gallery {
  position: relative;
  display: flex;
  z-index: 1;
  flex-direction: column;
}
.img {
  min-width: 100%;
  display: block;
  cursor: pointer;
}
.gallery__resize,
.gallery__resize:after {
  position: absolute;
  top: 0;
  cursor: pointer;
  height: 100%;
}
.gallery__resize {
  left: 0;
  width: 50%;
  overflow: hidden;
}
.tr {
  transition: 0.6s;
}
.gallery__resize:after {
  content: '';
  box-sizing: border-box;
  position: absolute;
  right: 0;
  z-index: 20;
}
#before {
  position: absolute;
  z-index: 100;
  font-size: 16px;
  padding: 10px 20px;
  bottom: 30px;
  text-align: left;
  transform: translateY(-50%);
  cursor: pointer;
  color: #fff;
  font-family: 'Open Sans', sans-serif;
  border-radius: 2px;
  right: 0;
}

@media (max-width: 768px) {
  #before {
    font-size: 1rem;
    padding: 8px 16px;
  }

  .blend-mode-luminosity {
    mix-blend-mode: luminosity;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .gallery {
    width: 350px;
  }
  .gallery__resize {
    width: 50%;
  }
  img {
    width: 350px;
  }
}
</style>
