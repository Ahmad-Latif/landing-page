<template>
  <div class="clients">
    <img class="clients__graphic" src="../assets/clients.png" />
    <div class="clients__content">
      <span class="clients__content__heading">
          Who we work with
      </span>
      <hr>
      <p class="clients__content__description">
        We are the trusted partner for customs matters of more than 7000 companies across Europe.
        Since 20 years we successfully operate with customers from small and large good owners
        to freight forwarders and digital platforms across various industries.
      </p>
    </div>
  </div>
</template>

<script>
export default {
name: "Clients"
}
</script>

<style scoped lang="scss">

.clients {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding: 20px;
  &__graphic {
    width: 40%;
    height: 281px;
    background-color: #F0F0F0;
  }
  &__content {
    width: 40%;
    &__heading {
      color: #3D4D62;
      font-size: 30px;
      font-weight: bold;
    }
    &__description {
      color: #3D4D62;
      font-size: 16px;
      font-weight: bold;
    }
  }
}

hr {
  height: 3px;
  background-color: #01A4B7;
  border: none;
  width: 10%;
  margin: 10px 0;
}

@media only screen and (max-width: 768px) {
  .clients {
    flex-direction:  column;
    &__graphic {
      height: auto;
      margin-bottom: 20px;
      width: 90%;
    }
    &__content {
      width: 90%;
    }
  }
}

</style>
