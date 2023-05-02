<template>
  <div class="book-now">
    <div class="book-now__container">
      <div class="book-now__container__top">
        <h2>Your Ultimate Skiing and Snowboarding Experience Starts Here</h2>
      </div>
      <div class="book-now__container__bottom">
        <div class="book-now__container__bottom__button">
          <button role="button" aria-label="Book Now">BOOK NOW</button>
        </div>
        <div class="book-now__container__bottom__images">
          <img
            class="book-now__container__bottom__images__snowflake"
            src="../assets/images/star.png"
            alt="visa"
          />
          <img src="../assets/images/image1.png" alt="Jump" />
          <img src="../assets/images/image2.png" alt="Friends" />
          <img src="../assets/images/image3.png" alt="Snowboard" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "BookNow",
};
</script>
<style lang="scss">
.book-now {
  width: 100%;
  background: #e5eaf5 0% 0% no-repeat padding-box;
  border-radius: 80px 80px 0px 0px;
  opacity: 1;
  height: 551px;
  position: relative;
  overflow: hidden;
  &__container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin: 30px;

    &__top {
      height: 100%;
      display: flex;
      justify-content: flex-start;
      align-items: flex-start;
      margin-top: 60px;
      h2 {
        width: 100%;
        text-align: left;
        font: normal normal 600 30px Montserrat;
        letter-spacing: 0.8px;
        color: #04080f;
        margin: 0;
      }
    }
    &__bottom {
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      flex-direction: column;
      &__button {
        margin: 25px 25px 0 0;
        button {
          width: 146px;
          height: 51px;
          background-color: #8806d0;
          border: none;
          border-radius: 26px;
          font-size: 16px;
          font-weight: 400;
          text-align: center;
          color: #ffffff;
          cursor: pointer;

          &:hover {
            background-color: #000000;
            color: #ffffff;
          }
        }
      }

      &__images {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        img {
          width: 116px;
          height: auto;
          border-radius: 10px 10px 0 0;
          margin: 30px 18px 30px 0;
          z-index: 2;
        }
        &__snowflake {
          width: 330px !important;
          height: 172px !important;
          color: #d6dce8;
          position: absolute;
          margin: 0 -40px 0 0 !important;
          right: 0;
          bottom: 0;
          z-index: 1;
        }
      }
    }
  }
}

// desktop styles
@media only screen and (min-width: 1280px) {
  .book-now {
    width: 100%;
    height: auto;
    background: #e5eaf5 0% 0% no-repeat padding-box;
    border-radius: 80px 80px 0px 0px;
    opacity: 1;
    &__container {
      height: auto;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin: 0 0 0 60px;
      &__top {
        width: 45%;
        height: auto;
        display: flex;
        justify-content: flex-start;
        align-items: flex-start;
        margin-top: 60px;
        h2 {
          width: 580px;
          height: 141px;
          /* UI Properties */
          font: var(--unnamed-font-style-normal) normal
            var(--unnamed-font-weight-600) var(--unnamed-font-size-40) /
            var(--unnamed-line-spacing-46) var(--unnamed-font-family-montserrat);
          letter-spacing: var(--unnamed-character-spacing-0-8);
          color: var(--unnamed-color-04080f);
          text-align: left;
          font: normal normal 600 40px/46px Montserrat;
          letter-spacing: 0.8px;
          color: #04080f;
          opacity: 1;
        }
      }
      &__bottom {
        height: auto;
        display: flex;
        justify-content: center;
        align-items: flex-start;
        flex-direction: row;

        &__button {
          margin: 25px 30px 0 0;
          button {
            width: 146px;
            height: 51px;
            /* UI Properties */
            background: var(--unnamed-color-8860d0) 0% 0% no-repeat padding-box;
            background: #8860d0 0% 0% no-repeat padding-box;
            border-radius: 26px;
            opacity: 1;
            cursor: pointer;

            &:hover {
              background-color: #000000;
              color: #ffffff;
            }
          }
        }

        &__images {
          display: flex;
          justify-content: space-between;
          align-items: center;
          height: 100%;
          overflow: hidden;
          img {
            width: 100%;
            height: auto;
            border-radius: 10px 10px 0 0;
            margin: 0px 20px;
          }
          &__snowflake {
            width: 422px !important;
            height: 277px !important;
            color: #d6dce8;
            margin: 0 -40px 0 0 !important;
            position: relative;
          }
        }
      }
    }
  }
}
</style>
