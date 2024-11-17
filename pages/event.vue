<template>
  <div>
    <NavTwo />
    <PageHeader title="All Events" />
    <Events />
    <CountdownTwo />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import PageHeader from "../components/PageHeader";
  import Events from "../components/Events";
  import CountdownTwo from "../components/CountdownTwo";
  import Footer from "../components/Footer";
  export default {
    components: {
      NavTwo,
      PageHeader,
      Events,
      CountdownTwo,
      Footer,
    },
    head(){
      return {
        title: "Potisen | All Events"
      }
    }
  }
</script>
