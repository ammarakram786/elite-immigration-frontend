<template>
  <div>
    <NavTwo />
    <PageHeader title="Event Details" />
    <EventDetails />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import PageHeader from "../components/PageHeader";
  import EventDetails from "../components/EventDetails";
  import Footer from "../components/Footer";
  export default {
    components: {
      NavTwo,
      PageHeader,
      EventDetails,
      Footer,
    },
    head(){
      return {
        title: "Potisen | Event Details"
      }
    }
  }
</script>
