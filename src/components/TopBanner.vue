<template>
  <div class="hero-image">
    <div class="hero-image-container">
      <div class="hero-image-info">
        <h1 class="hero-image-title">Plan the Perfect Adventure</h1>
        <p class="hero-image-text">
          Easily plan your ideal ski or snowboarding trip from home with the
          help of professionals.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopBanner",
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap");

$mobile-hero-image: "@/assets/images/mobile-hero.jpg";
$desktop-hero-image: "@/assets/images/Hero_Image.png";

.hero-image {
  height: 860px;
  background: #04080f url($mobile-hero-image) no-repeat center / cover;

  @media only screen and (min-width: 1280px) {
    margin-top: -80px;
    height: 956px;
    background: #04080f url($desktop-hero-image) no-repeat center / cover;
  }

  &-container {
    width: 100%;
    height: 100%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    @media only screen and (min-width: 1280px) {
      width: 500px;
      justify-content: center;
    }
  }

  &-info {
    margin-top: 150px;
    width: 300px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    @media only screen and (min-width: 1280px) {
      width: 500px;
      justify-content: center;
      margin-top: 420px;
    }
  }

  &-title {
    width: 300px;
    height: 73px;
    text-align: center;
    font: 600 30px/36px Montserrat;
    letter-spacing: 0.6px;
    color: #04080f;
    opacity: 1;
    margin-bottom: 0;

    @media only screen and (min-width: 1280px) {
      font: bold 50px Montserrat, sans-serif;
      letter-spacing: 1.5px;
      opacity: 1;
      width: 500px;
      margin: 30px auto 20px;
    }
  }

  &-text {
    font: lighter 20px Montserrat, sans-serif;
    color: #000000;
    text-align: center;
    letter-spacing: 0.4px;
    margin: 10px auto;

    @media only screen and (min-width: 1280px) {
      font-size: 20px;
      margin-top: 50px;
    }
  }
}
</style>
