<template>
  <div>
    <NavTwo />
    <PageHeader title="History" />
    <History />
    <FunFactOne />
    <CallToActionOne />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import PageHeader from "../components/PageHeader";
  import History from "../components/History";
  import CallToActionOne from "../components/CallToActionOne";
  import Footer from "../components/Footer";
  export default {
    components: {
      NavTwo,
      PageHeader,
      History,
      CallToActionOne,
      Footer,
    },
    head(){
      return {
        title: "Potisen | History"
      }
    }
  }
</script>
