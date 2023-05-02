<template>
  <div class="speak-to-agent">
    <div class="speak-to-agent-container">
      <div class="speak-to-agent-text">
        <h2>Unleash Your Inner Adventurer with Arctic Travel</h2>
        <p>
          Our team of expert travel agents are dedicated to helping you plan the
          trip of a lifetime, with a focus on both luxurious quality at the best
          possible price.
        </p>
      </div>
      <div class="speak-to-agent-image">
        <img src="@/assets/images/middleSnowflake.png" alt="Snowflake-image" />
      </div>
      <div class="speak-to-agent-contact">
        <p>
          Speak with one of our expert travel agents and start planning your
          dream skiing or snowboarding holiday. Let Arctic Travel take care of
          all the details, so that you can focus on what really matters -
          enjoying the trip of a lifetime.
        </p>
        <button class="speak-to-agent-button">Speak to an agent</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SpeakToAgent",
};
</script>

<style lang="scss">
.speak-to-agent {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.speak-to-agent-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90%;
  flex-direction: column;
  margin: auto 30px;
}

.speak-to-agent-text {
  width: 300px;
  text-align: start;
}

.speak-to-agent-text h2 {
  width: 100%;
  text-align: left;
  font: normal 600 30px Montserrat;
  letter-spacing: 0.6px;
  color: #04080f;
  opacity: 1;
  margin: 20px auto 0;
}

.speak-to-agent-image {
  width: 300px;
  height: auto;
  margin-bottom: 20px;
  img {
    width: 100%;
    height: auto;
  }
}

.speak-to-agent-contact {
  width: 300px;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-direction: column;
  text-align: center;
  p {
    text-align: start;
  }
}

.speak-to-agent-button {
  width: 214px;
  height: 51px;
  background-color: #8860d0;
  color: #ffffff;
  border: none;
  border-radius: 26px;
  font-size: 16px;
  font-weight: 700;
  margin: 5px 0 10px;
  cursor: pointer;
}

@media only screen and (min-width: 1280px) {
  .speak-to-agent-container {
    height: 398px;
    width: 1280px;
    margin: 80px 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: row;
  }

  .speak-to-agent-text {
    width: 400px;
    font: var(--unnamed-font-style-normal) normal
      var(--unnamed-font-weight-normal) var(--unnamed-font-size-20) /
      var(--unnamed-line-spacing-28) var(--unnamed-font-family-montserrat);
  }

  .speak-to-agent-text h2 {
    font: var(--unnamed-font-style-normal) normal var(--unnamed-font-weight-600)
      var(--unnamed-font-size-40) / var(--unnamed-line-spacing-46)
      var(--unnamed-font-family-montserrat);
  }

  .speak-to-agent-button {
    font: var(--unnamed-font-style-normal) normal
      var(--unnamed-font-weight-medium) var(--unnamed-font-size-16) /
      var(--unnamed-line-spacing-24) var(--unnamed-font-family-montserrat);
  }
  .speak-to-agent-image {
    width: 398px;
  }
  .speak-to-agent-contact {
    margin-left: 20px;
    width: 400px;
    font: var(--unnamed-font-style-normal) normal var(--unnamed-font-weight-300)
      var(--unnamed-font-size-16) / var(--unnamed-line-spacing-24)
      var(--unnamed-font-family-montserrat);
  }
}
</style>
