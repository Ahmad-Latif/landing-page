<template>
  <div>

  <!-- Navbar for desktop-->

    <div class="navbar desktop">
      <div class="navbar__left">
        <div class="navbar__logo__outer">
          <img class="navbar__logo" src="../assets/Logo.png" />
        </div>
        <div class="navbar__links">
          <div class="navbar__link">
            <span class="navbar__link__text" > Quick Facts </span>
            <span class="navbar__link__caret"> &#94; </span>
          </div>
          <div class="navbar__link">
            <span class="navbar__link__text" > Benefits </span>
            <span class="navbar__link__caret"> &#94; </span>
          </div>
          <span class="navbar__link__text"> Contact </span>
        </div>
      </div>
      <button class="navbar__right__button"> Get in touch </button>
    </div>

    <!-- Navbar for desktop-->

    <!-- Mobile Navbar Controls -->

    <div class="mobile__navbar__controls">
      <div class="navbar__logo__outer">
        <img class="navbar__logo" src="../assets/Logo.png" />
      </div>
      <span class="mobile__navbar__controls__icon" v-if="!openNavbar" @click="openNavbar = true" > &#9776; </span>
      <span class="mobile__navbar__controls__icon" v-else @click="openNavbar = false" > &#9747; </span>
    </div>

    <!-- Mobile Navbar Controls -->

    <!-- Mobile Navbar -->

    <div class="mobile__navbar" v-if="openNavbar">
      <div class="mobile__navbar__links">
        <span class="mobile__navbar__link"> Quick Facts </span>
        <hr style="width:50%">
        <span class="mobile__navbar__link"> Benefits </span>
        <hr style="width:50%">
        <span class="mobile__navbar__link"> Contact </span>
      </div>
    </div>

    <!-- Mobile Navbar -->
  </div>
</template>

<script>
export default {
name: "Navbar",
  data () {
    return {
      openNavbar : false
    }
  }
}
</script>

<style scoped lang="scss">
.navbar {
  height: 80px;
  background-color: white;
  opacity: 1;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 10px;
  &__left {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &__logo {
    width: 80%;
    &__outer {
      border-right: 3px solid lightgray;
    }
  }
  &__links {
    display: flex;
    align-items: center;
  }
  &__link {
    display: flex;
    align-items: center;
    margin: 0 20px;
    &__caret {
      transform: rotate(180deg);
      margin-top: -5px;
      margin-left: 5px;
      color: #01A4B7;
      font-weight: bold;
    }
    &__text {
      font-size: 12px;
      font-weight: bold;
      color: #3D4D62;
      &:hover {
        color: #01A4B7;
        cursor: pointer;
      }
    }
  }
  &__right__button {
    width: 151px;
    height: 50px;
    color: white;
    background-color: #01A4B7;
    border: unset;
    border-radius: 3px;
    &:hover {
      cursor: pointer;
      background-color: #006B6E;
    }
  }
}

.mobile__navbar__controls {
  display: none;
  margin: 0 10px;
  height: 80px;
}

.mobile__navbar {
  display: none;
  z-index: 1;
  height: 100vh;
  background-color: white;
  &__links {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  &__link {
    margin: 15px auto;
    font-size: 12px;
    font-weight: bold;
    color: #3D4D62;
    &:hover {
      color: #01A4B7;
      cursor: pointer;
    }
  }
}

@media only screen and (max-width: 768px) {
  .desktop {
    display: none;
  }
  .mobile__navbar__controls {
    display: flex;
    justify-content: space-between;
    align-items: center;
    &__icon {
      font-size: 30px;
      font-weight: bold;
      color: #01A4B7;
    }
  }
  .mobile__navbar {
    display: block;
  }
}


</style>
