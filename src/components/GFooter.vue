<template>
  <div class="footer">
    <div class="footer__links">
      <span class="footer__link"> Imprint </span>
      <span class="footer__link"> Data Security </span>
      <span class="footer__link"> Conditions </span>
      <span class="footer__link"> Cookies </span>
      <span class="footer__link"> Custom Support </span>
    </div>
    <div class="footer__license">
      <span>
      © 2021 Customs Support Group. All rights reserved.
    </span>
    </div>
  </div>
</template>

<script>
export default {
name: "GFooter"
}
</script>

<style scoped lang="scss">
.footer {
  margin: 15px 20%;
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  &__link {
    font-size: 12px;
    font-weight: bold;
    color: #3D4D62;
    margin: 0 5px;
    &:hover {
      color: #01A4B7;
      cursor: pointer;
    }
  }
  &__license {
    font-size: 12px;
    color: #445667;
  }
}

@media only screen and (max-width: 768px) {
  .footer {
    margin: 0 10%;
    flex-direction: column;
    align-items: flex-start;
    &__links {
      width: 100%;
    }
    &__link {
      display: flex;
      flex-direction: column;
      margin: 15px auto;
      align-items: flex-start;
      border-bottom: 1px solid;
    }
  }
}
</style>
