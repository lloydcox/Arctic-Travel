<template>
  <div class="keep-scrolling">
    <div class="keep-scrolling-container">
      <div class="keep-scrolling-image">
        <img src="../assets/images/keep-scrolling.png" alt="keep scrolling" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "KeepScrolling",
};
</script>
<style lang="scss">
.keep-scrolling {
  width: 100%;
  margin-top: -150px;
}

.keep-scrolling-container {
  position: relative;
}

.keep-scrolling-image {
  position: absolute;
  width: 110px;
  height: 110px;
  max-width: 110px;
  max-height: 110px;
  top: -15vh;
  left: 50%;
  transform: translateX(-50%);
  z-index: 5;
}

.keep-scrolling-image img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

@media only screen and (min-width: 1280px) {
  .keep-scrolling {
    margin-top: 0;
  }

  .keep-scrolling-image {
    top: -27vh;
    z-index: 5;
    right: 0vw;
    left: auto;
  }
}
</style>
