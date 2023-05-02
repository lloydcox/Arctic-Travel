<template>
  <div class="header-menu">
    <div class="header-menu-container">
      <div class="header-menu-left">
        <img
          class="logo"
          :src="require('@/assets/images/Logo.png')"
          alt="logo"
        />
      </div>
      <div class="header-menu-right">
        <div class="header-menu-button">
          <img src="@/assets/images/burger-menu.png" alt="menu" />
        </div>
        <!-- button to change language -->
        <button class="header-menu-right-language" @click="changeLanguage">
          <img :src="require('@/assets/images/Globe.png')" alt="language" />
          <span>{{ language }}</span>
        </button>
        <!-- button to redirect to My Trips page -->
        <button
          class="header-menu-right-my-trips"
          @click="redirectTo('/my-trips')"
        >
          <span>My trips</span>
        </button>
        <!-- button to redirect to Sign In page -->
        <button
          class="header-menu-right-sign-in"
          @click="redirectTo('/sign-in')"
        >
          <span>Sign in</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderMenu",
  data() {
    return {
      language: "English", //default language is English
    };
  },
  methods: {
    redirectTo(path) {
      /* Function to redirect to different pages based on the button clicked */
      this.$router.push(path);
    },
    changeLanguage() {
      // code to change language goes here
      this.language = "French"; //example for changing the language to French
    },
  },
};
</script>

<style scoped>
/* styles for mobile */
.header-menu {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  z-index: 5;
}
.header-menu-container {
  margin: 20px 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header-menu-left {
  width: 75%;
  text-align: left;
}
.logo {
  width: 192px;
  height: 60px;
}

.header-menu-right-my-trips,
.header-menu-right-sign-in,
.header-menu-right-language {
  display: none;
}

/* styles for desktop */
@media only screen and (min-width: 1280px) {
  .header-menu {
    position: absolute;
    top: 0px;
    left: 0px;
    width: 100%;
    height: 60px;
    z-index: 5;
  }
  .header-menu-container {
    margin: 60px;
    height: 60px;
    opacity: 1;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 1;
  }

  .header-menu-button {
    display: none;
  }

  .header-menu-left {
    display: flex;
    align-items: center;
  }

  .header-menu-right {
    width: 25%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .header-menu-right-language {
    display: flex;
    align-items: center;
    padding: 0;
    background-color: transparent;
    border: none;
    cursor: pointer;
    font-size: 16px;
  }

  .header-menu-right-language img {
    height: 20px;
    width: 20px;
    margin-right: 10px;
  }

  .header-menu-right-my-trips,
  .header-menu-right-sign-in {
    display: block;
    background-color: transparent;
    border: none;
    cursor: pointer;
    font-size: 16px;
  }

  .header-menu-right-my-trips span,
  .header-menu-right-sign-in span,
  .header-menu-right-language span {
    text-align: center;
    font: normal 16px Montserrat;
    letter-spacing: 0.32px;
    color: #04080f;
    opacity: 1;
    margin: 0 5px;
  }
}
</style>
