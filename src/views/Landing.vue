<template>
  <div>
    <Header/>
    <Clients/>
    <LeadingCustomers/>
    <Gallery/>
  </div>
</template>

<script>
import Header from "../components/Header";
import Clients from "../components/Clients";
import LeadingCustomers from "../components/LeadingCustomers";
import Gallery from "../components/Gallery";
export default {
name: "Landing",
  components : {
    Header , Clients , LeadingCustomers , Gallery
  }
}
</script>

<style scoped>

</style>
