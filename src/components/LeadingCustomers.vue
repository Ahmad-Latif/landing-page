<template>
  <div class="customers">
    <span class="customers__heading"> The leading customs agent in Europe and UK </span>
    <hr>
    <div class="customers__detail">
      <div class="customers__detail__sub" v-for="(customer, index) in customersData" :key="index">
        <span class="customers__detail__number"> {{customer.number}} </span>
        <span  class="customers__detail__text"> {{customer.text}} </span>
      </div>
    </div>
    <button class="customers__btn">
      Get in touch
    </button>
  </div>
</template>

<script>
export default {
  name: "LeadingCustomers",
  data () {
    return {
      customersData : [
        {
          number : '20 +',
          text : 'years of experience'
        },
        {
          number : '400',
          text : 'qualified customs specialists'
        },
        {
          number : '200',
          text : 'strategic locations'
        },
        {
          number : '5',
          text : 'countries'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">

.customers {
  background-color: #006B6E;
  min-height: 438px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  &__heading {
    font-size: 40px;
    font-weight: bold;
    color: white;
  }
  &__detail {
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    &__sub {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      margin: 20px 20px;
      border-right: 3px solid lightgray;
      padding: 10px;
      &:last-child {
        border: none;
      }
    }
    &__number {
      font-size: 50px;
      font-weight: bold;
    }
    &__text {
      font-size: 20px;
      font-weight: bold;
      text-align: center;
    }
  }
  &__btn {
    width: 151px;
    height: 50px;
    color: white;
    background-color: #01A4B7;
    border: unset;
    border-radius: 3px;
    margin-top: 20px;
    font-size: 18px;
    font-weight: bold;
    &:hover {
      cursor: pointer;
      color: #01A4B7;
      background-color: white;
    }
  }
}

hr {
  height: 3px;
  background-color: #01A4B7;
  border: none;
  width: 5%;
  margin: 10px auto;
}

@media only screen and (max-width: 768px) {
  .customers {
    padding: 30px;
    &__heading {
      text-align: center;
    }
    &__detail {
      flex-direction: column;
      &__sub {
        border-right: unset;
        border-bottom : 3px solid lightgray;
        width: 100%;
      }
    }
  }
}


</style>
