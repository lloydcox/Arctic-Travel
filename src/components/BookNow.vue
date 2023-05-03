<template>
  <div class="book-now">
    <div class="book-now__container">
      <div class="book-now__container__top">
        <h2>Your Ultimate Skiing and Snowboarding Experience Starts Here</h2>
      </div>
      <div class="book-now__container__bottom">
        <div
          class="book-now__container__bottom__button"
          role="button"
          aria-label="Book Now"
        >
          BOOK NOW
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
  margin-top: 20px;
  &__container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin: 25px 30px;

    &__top {
      height: 100%;
      display: flex;
      justify-content: flex-start;
      align-items: flex-start;
      h2 {
        font: var(--unnamed-font-style-normal) normal
          var(--unnamed-font-weight-600) 30px/36px
          var(--unnamed-font-family-montserrat);
        color: var(--unnamed-color-04080f);
        text-align: left;
        font: normal normal 600 30px/36px Montserrat;
        letter-spacing: 0.6px;
      }
    }
    &__bottom {
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      flex-direction: column;
      margin-top: 5px;
      &__button {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 146px;
        height: 51px;
        background: var(--unnamed-color-8860d0) 0% 0% no-repeat padding-box;
        border-radius: 26px;
        font: var(--unnamed-font-style-normal) normal
          var(--unnamed-font-weight-medium) var(--unnamed-font-size-16) /
          var(--unnamed-line-spacing-24) var(--unnamed-font-family-montserrat);
        letter-spacing: var(--unnamed-character-spacing-0-32);
        color: var(--unnamed-color-ffffff);
        text-align: center;
        cursor: pointer;
        margin: 0;

        &:hover {
          background-color: #000000;
          color: #ffffff;
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
          width: 300px !important;
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
