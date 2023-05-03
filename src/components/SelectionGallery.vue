<template>
  <div class="selection-gallery">
    <div class="selection-gallery-container">
      <div
        :class="[
          'selection-gallery-container__tabs',
          activeTab.name.toLowerCase(),
        ]"
      >
        <button
          class="selection-gallery-container__tabs__button--prev"
          @click="changeTab(-1)"
        ></button>
        <div
          class="selection-gallery-container__tabs__tab"
          v-for="tab in tabs"
          :key="tab.id"
          @click="changeTab(tab.id - currentTabId)"
          :class="{ active: tab.isActive }"
          :style="{
            display: isMobile ? (tab.isActive ? 'block' : 'none') : 'block',
          }"
        >
          {{ tab.name }}
        </div>

        <button
          class="selection-gallery-container__tabs__button--next"
          @click="changeTab(1)"
        ></button>
      </div>

      <div class="selection-gallery-container__images">
        <div class="selection-gallery-container__images__container">
          <div
            class="selection-gallery-container__images__container__image"
            v-for="image in activeImages"
            :key="image.id"
          >
            <img :src="image.src" :alt="image.alt" />
            <h5>{{ image.description }}</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import region1 from "../assets/images/selection-gallery/regions/1.png";
import region2 from "../assets/images/selection-gallery/regions/2.png";
import region3 from "../assets/images/selection-gallery/regions/3.png";
import region4 from "../assets/images/selection-gallery/regions/4.png";
import region5 from "../assets/images/selection-gallery/regions/5.png";
import region6 from "../assets/images/selection-gallery/regions/6.png";
import region7 from "../assets/images/selection-gallery/regions/7.png";

export default {
  name: "SelectionGallery",
  data() {
    return {
      tabs: [
        {
          id: 1,
          name: "Regions",
          images: [
            {
              id: 1,
              src: region1,
              alt: "Aerial view of a ski resort",
              description: "I'm flexible",
            },
            {
              id: 2,
              src: region2,
              alt: "Aerial view of a ski resort",
              description: "Europe",
            },
            {
              id: 3,
              src: region3,
              alt: "Aerial view of a ski resort",
              description: "Canada",
            },
            {
              id: 4,
              src: region4,
              alt: "Aerial view of a ski resort",
              description: "United States",
            },
            {
              id: 5,
              src: region5,
              alt: "Aerial view of a ski resort",
              description: "South America",
            },
            {
              id: 6,
              src: region6,
              alt: "Aerial view of a ski resort",
              description: "Japan",
            },
            {
              id: 7,
              src: region7,
              alt: "Aerial view of a ski resort",
              description: "Oceania",
            },
          ],
          isActive: true,
        },
        {
          id: 2,
          name: "Resorts",
          images: [
            {
              id: 1,
              src: require("../assets/images/selection-gallery/regions/1.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 2,
              src: require("../assets/images/selection-gallery/regions/2.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 3,
              src: require("../assets/images/selection-gallery/regions/3.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 4,
              src: require("../assets/images/selection-gallery/regions/4.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 5,
              src: require("../assets/images/selection-gallery/regions/5.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 6,
              src: require("../assets/images/selection-gallery/regions/6.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 7,
              src: require("../assets/images/selection-gallery/regions/7.png"),
              alt: "Aerial view of a ski resort",
            },
          ],
          isActive: false,
        },
        {
          id: 3,
          name: "Lodgings",
          images: [
            {
              id: 1,
              src: require("../assets/images/selection-gallery/regions/1.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 2,
              src: require("../assets/images/selection-gallery/regions/2.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 3,
              src: require("../assets/images/selection-gallery/regions/3.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 4,
              src: require("../assets/images/selection-gallery/regions/4.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 5,
              src: require("../assets/images/selection-gallery/regions/5.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 6,
              src: require("../assets/images/selection-gallery/regions/6.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 7,
              src: require("../assets/images/selection-gallery/regions/7.png"),
              alt: "Aerial view of a ski resort",
            },
          ],
          isActive: false,
        },
        {
          id: 4,
          name: "Passes",
          images: [
            {
              id: 1,
              src: require("../assets/images/selection-gallery/regions/1.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 2,
              src: require("../assets/images/selection-gallery/regions/2.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 3,
              src: require("../assets/images/selection-gallery/regions/3.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 4,
              src: require("../assets/images/selection-gallery/regions/4.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 5,
              src: require("../assets/images/selection-gallery/regions/5.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 6,
              src: require("../assets/images/selection-gallery/regions/6.png"),
              alt: "Aerial view of a ski resort",
            },
            {
              id: 7,
              src: require("../assets/images/selection-gallery/regions/7.png"),
              alt: "Aerial view of a ski resort",
            },
          ],
          isActive: false,
        },
      ],
      currentTabId: 1,
      isMobile: false,
    };
  },
  computed: {
    activeTab() {
      return this.tabs.find((tab) => tab.id === this.currentTabId);
    },
    activeImages() {
      return this.activeTab.images;
    },
  },
  methods: {
    changeTab(change) {
      const newIndex = this.currentTabId + change;
      if (newIndex >= 1 && newIndex <= this.tabs.length) {
        this.currentTabId = newIndex;
        this.tabs.forEach((tab) => {
          tab.isActive = tab.id === this.currentTabId;
        });
      }
    },
  },

  mounted() {
    const setDisplay = () => {
      this.isMobile = window.innerWidth < 768;
      const tab = {
        isActive: this.activeTab.id === 1,
      };
      if (this.isMobile) {
        document.getElementsByClassName("active")[0].style.display =
          tab.isActive ? "block" : "none";
      } else {
        const tabs = document.getElementsByClassName(
          "selection-gallery-container__tabs__tab"
        );
        for (let i = 0; i < tabs.length; i++) {
          tabs[i].style.display = "block";
        }
      }
    };
    window.addEventListener("resize", setDisplay);
    setDisplay();
  },
};
</script>

<style lang="scss">
// mobile styles
.selection-gallery {
  width: 100%;
  margin-top: -175px;
  background: #e5eaf5;
  opacity: 1;
  z-index: 2;
  border-radius: 80px 80px 0 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  padding-bottom: 30px;
  .selection-gallery-container {
    width: 90%;
    height: 100%;
    top: 10;
    left: 0;
    opacity: 1;
    margin-top: 50px;
    display: flex;
    flex-direction: column;
    &__tabs {
      justify-content: space-around;
      flex-direction: row;
      align-items: center;
      width: 100%;
      height: 4.3em;
      background: #fff;
      margin: 40px auto 0;
      border-radius: 20px 20px 0 0;
      opacity: 1;
      display: flex;
      &__tab {
        border-radius: 26px;
        text-align: center;
        font: normal 24px Montserrat;
        letter-spacing: 0.32px;
        color: #04080f;
        cursor: pointer;
      }
      &__button--next {
        width: 43px;
        height: 43px;
        background: #fff;
        border-radius: 50%;
        opacity: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        &::after {
          content: "";
          display: inline-block;
          width: 15px;
          height: 25px;
          background: url("@/assets/images/selection-gallery/Arrow.svg")
            no-repeat;
          background-size: 100%;
          vertical-align: middle;
          color: #000;
          filter: invert(1);
          transform: rotate(270deg);
        }
      }
      &__button--prev {
        width: 43px;
        height: 43px;
        background: #fff;
        border-radius: 50%;
        opacity: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        &::after {
          content: "";
          display: inline-block;
          width: 15px;
          height: 25px;
          background: url("@/assets/images/selection-gallery/Arrow.svg")
            no-repeat;
          background-size: 100%;
          vertical-align: middle;
          color: #000;
          filter: invert(1);
          transform: rotate(90deg);
        }
      }
    }
    &__images {
      width: 100%;
      height: 100%;
      background: #fff;
      border-radius: 0 0 20px 20px;
      opacity: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      &__container {
        width: 95%;
        background: #fff;
        border-radius: 0 0 20px 20px;
        opacity: 1;
        display: flex;
        flex-direction: column;
        align-items: center;
        flex-wrap: wrap;
        &__image {
          width: 100%;
          background: #fff;
          border-radius: 0 0 20px 20px;
          opacity: 1;
          display: flex;
          flex-direction: column;
          align-items: center;
          & img {
            width: 100%;
          }
          & h5 {
            width: 100%;
            margin: 10px 0 20px;
            text-align: start;
          }
        }
      }
    }
  }
}

@media only screen and (min-width: 1280px) {
  .selection-gallery {
    margin-top: -100px;
    .selection-gallery-container {
      width: 1400px;
      height: 664px;
      top: 0;
      left: 0px;
      opacity: 1;
      margin-top: 40px;
      display: flex;
      flex-direction: column;
      &__tabs {
        justify-content: space-around;
        align-items: center;
        width: 620px;
        height: 4.3em;
        background: #fff;
        margin: 0 auto;
        border-radius: 20px 20px 0 0;
        opacity: 1;
        display: flex;
        &__tab {
          display: block !important;
          width: 100px;
          padding: 0.5em 1em;
          border-radius: 26px;
          margin-right: 0;
          text-align: center;
          cursor: pointer;
          background-color: transparent;
          &:hover {
            background-color: #5ab9ea;
            color: #fff;
          }
        }
        &__button--prev {
          display: none;
        }
        &__button--next {
          display: none;
        }
      }

      &__images {
        display: flex;
        justify-content: center;
        width: 1280px;
        height: 550px;
        top: 742px;
        left: 60px;
        margin: 0 auto;
        border-radius: 15px;
        background: #fff;

        &__container {
          display: flex;
          justify-content: flex-start;
          flex-direction: row;
          flex-wrap: wrap;
          width: 1256px;
          position: relative;
          height: 485px;
          // top: 742px;
          // left: 60px;
          border-radius: 5px;
          margin-top: 10px;
          background: #fff;

          &__image {
            width: auto;
            margin: 13px;
            border-radius: 5px;
            img {
              width: 288px;
              height: 200px;
              object-fit: cover;
            }
            h5 {
              width: auto;
              margin: 5px auto;
              text-align: left;
              color: #04080f;
              font: normal normal normal 16px/24px Montserrat;
              letter-spacing: 0.32px;
            }
          }
        }
      }
    }
  }
}
</style>
