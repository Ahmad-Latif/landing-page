<template>
  <div class="header">
    <div class="header__heading">
      <span class="header__main__heading">
        Headache on complex customs matters for your business?
      </span>
      <hr>
      <p class="header__description">
        Customs Support is your neutral full-service customs broker for complex customs matters with 20+ years of
        expertise in Europe and over 400 customs specialists who are happy to take the load off your mind!
      </p>
      <button class="header__btn desktop">
        Get your quote now
      </button>
    </div>
    <div class="header__features">
      <p>
        <span class="header__features__icon"> &#10004; </span>
        <span class="header__features__text"> Fast and accurate customs clearance delivery </span>
      </p>
      <p>
        <span class="header__features__icon"> &#10004; </span>
        <span class="header__features__text"> EU-wide customs coverage </span>
      </p>
      <p>
        <span class="header__features__icon"> &#10004; </span>
        <span class="header__features__text"> Online and real-time control of customs processes </span>
      </p>
    </div>
    <button class="header__btn mobile">
      Get your quote now
    </button>

  </div>
</template>

<script>
export default {
name: "Header"
}
</script>

<style scoped lang="scss">

.header {
  background: url("../assets/hero.png");
  background-position-x: center;
  height: 690px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  &__heading {
    width: 45%;
  }
  &__main__heading {
    font-size: 40px;
    color: white;
    text-align: left;
  }
  &__description {
    color: white;
    font-size: 16px;
  }
  &__btn {
    width: 206px;
    height: 50px;
    color: white;
    background-color: #01A4B7;
    border: unset;
    border-radius: 3px;
    margin-top: 20px;
    &:hover {
      cursor: pointer;
    }
  }
  &__features {
    width: 30%;
    margin-left: 5%;
    &__icon {
      color: #01A4B7;
      font-size: 20px;
    }
    &__text {
      color: white;
    }
  }
}

.mobile {
  display: none;
}

hr {
  height: 3px;
  background-color: #01A4B7;
  border: none;
  width: 10%;
  margin: 10px 0;
}

@media only screen and (max-width: 768px) {
  .header {
    flex-direction: column;
    justify-content: center;
    height: auto;
    padding: 20px;
    &__features {
      width: 50%;
    }
  }
  .desktop {
    display: none;
  }
  .mobile {
    display: block;
  }
}

@media only screen and (max-width: 425px) {
  .header__heading ,
  .header__features {
    width: 90%;
  }
}
</style>
