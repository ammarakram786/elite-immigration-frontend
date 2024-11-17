<template>
  <div>
    <NavTwo />
    <PageHeader title="Donation" />
    <Donation />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import PageHeader from "../components/PageHeader";
  import Donation from "../components/Donation";
  import Footer from "../components/Footer";
  export default {
    components: {
      NavTwo,
      PageHeader,
      Donation,
      Footer,
    },
    head(){
      return {
        title: "Potisen | Donation"
      }
    }
  }
</script>
