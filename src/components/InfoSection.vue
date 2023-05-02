<!-- In this component we create a component that is split into left and right parts
  the left side has a h2 title "Choose Arctic Travel for a Hassle-Free, Customisable, 
  and Affordable Holiday" it then has 3 list items, each has an image to te left, then
   a sentence to the right of it the image and senetence are in the information object 
   lastly underneath the three items is a "speak to an agent" button
on the right of the page is an image that takes up the full height of the section and the right side
  -->
<template>
  <div class="info-section" aria-label="Arctic Travel information">
    <div class="info-section__container">
      <div class="info-section__container__left">
        <h2>
          Choose Arctic Travel for a Hassle-Free, Customisable, and Affordable
          Holiday
        </h2>
        <ul>
          <li v-for="info in information" :key="info.id">
            <img :src="info.image" alt="info" />
            <p>{{ info.text }}</p>
          </li>
        </ul>
        <div class="info-section__container__left__button">
          <button
            class="info-section__container__left__button__but"
            role="button"
            aria-label="Speak to an agent"
          >
            SPEAK TO AN AGENT
          </button>
        </div>
      </div>
      <div class="info-section__container__right">
        <img src="../assets/images/snowboard.png" alt="snowboard" />
      </div>
    </div>
  </div>
</template>
<script>
import ski from "@/assets/images/Ski_Icon.png";
import airplane from "@/assets/images/Airplane_Icon.png";
import money from "@/assets/images/Money_Icon.png";

export default {
  name: "InfoSection",
  data() {
    return {
      information: [
        {
          id: 1,
          image: ski,
          text: "We helps skiers and snowboarders find their ideal destination regardless of skill level and preferences.",
        },
        {
          id: 2,
          image: airplane,
          text: "We provide attention to every detail of the trip, from flights and transfers to accommodation, equipment rental, and dining reservations.",
        },
        {
          id: 3,
          image: money,
          text: "We are committed to offering the best possible prices through exclusive deals and discounts from our network of travel partners.",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.info-section {
  width: 100%;
  display: flex;
  justify-content: center;
  &__container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 30px;
    &__left {
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: flex-start;
      h2 {
        font: var(--unnamed-font-style-normal) normal
          var(--unnamed-font-weight-600) var(--unnamed-font-size-40) /
          var(--unnamed-line-spacing-46) var(--unnamed-font-family-montserrat);
        letter-spacing: var(--unnamed-character-spacing-0-8);
        color: var(--unnamed-color-04080f);
        text-align: left;
        margin: auto;
        margin-bottom: 20px;
      }
      ul {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        list-style: none;
        margin: 0;
        padding: 0;
        li {
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          align-items: start;
          img {
            width: 60px;
            height: 60px;
          }
          p {
            font: var(--unnamed-font-style-normal) normal
              var(--unnamed-font-weight-300) var(--unnamed-font-size-16) /
              var(--unnamed-line-spacing-24)
              var(--unnamed-font-family-montserrat);
            letter-spacing: var(--unnamed-character-spacing-0-32);
            color: var(--unnamed-color-04080f);
            text-align: left;
          }
        }
      }
      &__button {
        &__but {
          border-radius: 26px;
          width: 214px;
          height: 51px;
          background-color: #8860d0;
          font: var(--unnamed-font-style-normal) normal
            var(--unnamed-font-weight-medium) var(--unnamed-font-size-16) /
            var(--unnamed-line-spacing-24) var(--unnamed-font-family-montserrat);
          letter-spacing: var(--unnamed-character-spacing-0-32);
          color: var(--unnamed-color-ffffff);
          text-align: center;
          cursor: pointer;
        }
      }
    }
    &__right {
      display: flex;
      width: 100%;
      height: auto;
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 30px;
      img {
        width: 100%;
        height: auto;
      }
    }
  }
}

@media only screen and (min-width: 1280px) {
  .info-section {
    &__container {
      flex-direction: row;
      justify-content: space-between;
      width: 100%;
      margin: 60px;
      &__left {
        width: 45%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: flex-start;
        h2 {
          width: 600px;
          font-size: 40px;
          font-weight: 700;
          line-height: 1.2;
          margin: 0 0 20px 0;
        }
        ul {
          margin: 0;
          padding: 0;
          li {
            flex-direction: row;
            align-items: center;
            margin-bottom: 10px;
            img {
              width: 60px;
              height: 60px;
            }
            p {
              width: 90%;
              font-size: 18px;
              font-weight: 400;
              line-height: 1.5;
              text-align: left;
              margin-left: 20px;
            }
          }
        }
        &__button {
          button {
            width: 214px;
            height: 51px;
            background-color: #8860d0;
            color: #ffffff;
            border: none;
            border-radius: 26px;
            font-size: 16px;
            margin-top: 20px;
            cursor: pointer;
          }
        }
      }
      &__right {
        margin: 0;
        width: 45%;
      }
    }
  }
}
</style>
