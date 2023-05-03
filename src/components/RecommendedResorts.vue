<template>
  <div class="carousel__container">
    <div class="carousel__title">
      <h1>Recommended Resorts</h1>
    </div>
    <div class="carousel__paragraph">
      <h3>
        We have carefully curated a collection of the finest ski resorts around
        the world, from the snow-capped peaks of the Alps to the rugged beauty
        of the Rockies.
      </h3>
    </div>
    <div class="vueper-container">
      <vueper-slides
        class="no-shadow"
        :visible-slides="3"
        arrowsOutside="true"
        :gap="2"
        :breakpoints="breakpoints"
        :bullets="false"
      >
        <vueper-slide
          class="vueperslide"
          v-for="slide in slides"
          :key="slide.id"
        >
          <template #content>
            <div class="carousel__item__container">
              <div class="carousel__item__image">
                <img :src="slide.src" :alt="slide.alt" />
              </div>
              <div class="carousel__item__details">
                <h2>{{ slide.name }}</h2>
                <p>{{ slide.description }}</p>
              </div>
            </div>
          </template>
        </vueper-slide>
      </vueper-slides>
    </div>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";

// Import the image sources
import region1 from "@/assets/images/selection-gallery/regions/1.png";
import region2 from "@/assets/images/selection-gallery/regions/2.png";
import region3 from "@/assets/images/selection-gallery/regions/3.png";
import region4 from "@/assets/images/selection-gallery/regions/4.png";
import region5 from "@/assets/images/selection-gallery/regions/5.png";
import region6 from "@/assets/images/selection-gallery/regions/6.png";
import region7 from "@/assets/images/selection-gallery/regions/7.png";

export default {
  name: "RecommendedResorts",
  components: {
    VueperSlides,
    VueperSlide,
  },
  data: () => ({
    slides: [
      {
        id: 1,
        src: region1, 
        alt: "Aerial view of a ski resort",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        name: "USA Resort Colorado",
      },
      {
        id: 2,
        src: region2,
        alt: "Aerial view of a ski resort",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        name: "Europe Resort",
      },
      {
        id: 3,
        src: region3,
        alt: "Aerial view of a ski resort",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        name: "Canada Resort",
      },
      {
        id: 4,
        src: region4,
        alt: "Aerial view of a ski resort",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        name: "USA Resort 2",
      },
      {
        id: 5,
        src: region5,
        alt: "Aerial view of a ski resort",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        name: "South America Resort",
      },
      {
        id: 6,
        src: region6,
        alt: "Aerial view of a ski resort",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        name: "Japan Resort",
      },
      {
        id: 7,
        src: region7,
        alt: "Aerial view of a ski resort",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        name: "New Zealand Resort",
      },
    ],
    breakpoints: {
      1200: {
        slideRatio: 1 / 3,
        visibleSlides: 2,
        gap: 2,
      },
      600: {
        slideRatio: 1 / 3,
        visibleSlides: 1,
        gap: 2,
      },
    },
  }),
};
</script>

<style lang="scss">
// Mobile styles
.carousel__container {
  height: 100%;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 30px;
}
.carousel__title {
  h1 {
    width: 300px;
    height: 73px;
    font: var(--unnamed-font-style-normal) normal var(--unnamed-font-weight-600)
      30px/36px var(--unnamed-font-family-montserrat);
    color: var(--unnamed-color-04080f);
    text-align: center;
    margin: 10px;
  }
}

.carousel__paragraph {
  h3 {
    width: 300px;
    height: 152px;
    /* UI Properties */
    font: var(--unnamed-font-style-normal) normal
      var(--unnamed-font-weight-normal) 18px/26px
      var(--unnamed-font-family-montserrat);
    color: var(--unnamed-color-04080f);
    text-align: center;
  }
}

.vueper-container {
  width: 90%;
  height: auto;
}

.vueperslides,
.vueperslides__inner,
.vueperslides__parallax-wrapper {
  width: 100%;
  height: 350px;
  padding-bottom: 0 !important;
}

.vueper {
  position: relative;
  width: 100%;
  overflow: visible;
  margin: 0 auto;
  height: auto;
}

.vueperslide {
  border-radius: 10px;
  background: var(--unnamed-color-ffffff) 0% 0% no-repeat padding-box;
}

.carousel__item__container {
  width: 80%;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: auto;
}

.carousel__item__image {
  width: 100%;
  height: 238px;
  border-radius: 10px;
  overflow: hidden;
  margin: 5px;
  img {
    width: 100%;
    height: 238px;
  }
}

.carousel__item__details {
  width: 361px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.carousel__item__details h2 {
  width: 186px;
  height: 19px;
  font: var(--unnamed-font-style-normal) normal
    var(--unnamed-font-weight-normal) var(--unnamed-font-size-16) /
    var(--unnamed-line-spacing-24) var(--unnamed-font-family-montserrat);
  letter-spacing: var(--unnamed-character-spacing-0-32);
  color: var(--unnamed-color-04080f);
  text-align: center;
}

.carousel__item__details p {
  width: 300px;
  height: 43px;
  /* UI Properties */
  font: var(--unnamed-font-style-normal) normal var(--unnamed-font-weight-300)
    var(--unnamed-font-size-16) / var(--unnamed-line-spacing-24)
    var(--unnamed-font-family-montserrat);
  letter-spacing: var(--unnamed-character-spacing-0-32);
  color: var(--unnamed-color-04080f);
  text-align: center;
}

.vueperslides__arrow--prev,
.vueperslides__arrow--next {
  width: 25px;
  height: 25px;
  color: #000;
  background-color: transparent;
  border-radius: 50%;
  border: 1px solid #000;
  position: absolute;
  transform: translateY(-50%) rotate(90deg);
  z-index: 10;
  top: 37.5%;
  left: -1em !important;
  right: auto !important;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
  svg {
    display: contents;
  }
}
.vueperslides__arrow--prev::after,
.vueperslides__arrow--next::after {
  content: "";
  display: inline-block;
  width: 14px;
  height: 20px;
  background: url("@/assets/images/selection-gallery/Arrow.svg") no-repeat;
  background-size: 100%;
  vertical-align: middle;
  color: #000;
  filter: invert(1); 
}
.vueperslides__arrow--next {
  transform: translateY(-50%) rotate(270deg);
  right: -1em !important;
  left: auto !important;
}
@media only screen and (min-width: 1280px) {
  .carousel__container {
    height: 100%;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .carousel__title {
    width: 638px;
    /* UI Properties */
    text-align: center;
    font-family: Montserrat;
    letter-spacing: 0.8px;
    color: #04080f;
    opacity: 1;
    margin: 0;
  }

  .carousel__title h1 {
    width: 638px;
    font: var(--unnamed-font-style-normal) normal var(--unnamed-font-weight-600)
      var(--unnamed-font-size-40) / var(--unnamed-line-spacing-46)
      var(--unnamed-font-family-montserrat);
    letter-spacing: var(--unnamed-character-spacing-0-8);
    color: var(--unnamed-color-04080f);
    text-align: center;
  }

  .carousel__paragraph h3 {
    width: 783px;
    font: var(--unnamed-font-style-normal) normal
      var(--unnamed-font-weight-normal) var(--unnamed-font-size-20) /
      var(--unnamed-line-spacing-28) var(--unnamed-font-family-montserrat);
    letter-spacing: var(--unnamed-character-spacing-0-4);
    color: var(--unnamed-color-04080f);
    text-align: center;
    margin-bottom: 40px;
    /* } */
  }

  .vueper-container {
    width: 1200px;
    height: 100%;
  }

  .vueper {
    position: relative;
    width: 1143px;
    overflow: visible;
    margin: 0 auto;
  }

  .vueperslides,
  .vueperslides__inner,
  .vueperslides__parallax-wrapper {
    width: 100%;
    height: 500px;
    padding-bottom: 0 !important;
  }

  .vueperslide {
    border-radius: 10px;
    background-color: #ffffff;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .carousel__item__container {
    width: 361px;
    height: 500px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .carousel__item__image {
    width: 361px;
    height: auto;
    border-radius: 10px;
    overflow: hidden;
  }

  .carousel__item__image img {
    width: 100%;
    height: 414px;
  }

  .carousel__item__details {
    width: 361px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .carousel__item__details h2 {
    font: var(--unnamed-font-style-normal) normal
      var(--unnamed-font-weight-normal) var(--unnamed-font-size-16) /
      var(--unnamed-line-spacing-24) var(--unnamed-font-family-montserrat);
    letter-spacing: var(--unnamed-character-spacing-0-32);
    color: var(--unnamed-color-04080f);
    text-align: center;
  }

  .carousel__item__details p {
    font: var(--unnamed-font-style-normal) normal var(--unnamed-font-weight-300)
      var(--unnamed-font-size-16) / var(--unnamed-line-spacing-24)
      var(--unnamed-font-family-montserrat);
    letter-spacing: var(--unnamed-character-spacing-0-32);
    color: var(--unnamed-color-04080f);
    text-align: center;
    margin: 0 auto 30px;
  }

  .carousel {
    position: relative;
  }
  .vueperslides__arrow--prev,
  .vueperslides__arrow--next {
    width: 43px;
    height: 43px;
    color: var(--unnamed-color-000000);
    background-color: transparent;
    border-radius: 50%;
    border: 1px solid #000;
    position: absolute;
    transform: translateY(-50%) rotate(90deg);
    z-index: 10;
    top: 42.5%;
    left: -3em !important;
    right: auto !important;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
    svg {
      display: contents;
    }
  }
  .vueperslides__arrow--prev::after,
  .vueperslides__arrow--next::after {
    content: "";
    display: inline-block;
    width: 14px;
    height: 20px;
    background: url("@/assets/images/selection-gallery/Arrow.svg") no-repeat;
    background-size: 100%;
    vertical-align: middle;
    color: #000;
    filter: invert(1);
  }
  .vueperslides__arrow--next {
    transform: translateY(-50%) rotate(270deg);
    right: -3em !important;
    left: auto !important;
  }
}
</style>
