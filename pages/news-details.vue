<template>
  <div>
    <NavTwo />
    <PageHeader title="News Details" />
    <NewsDetails />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import PageHeader from "../components/PageHeader";
  import NewsDetails from "../components/NewsDetails";
  import Footer from "../components/Footer";
  export default {
    components: {
      NavTwo,
      PageHeader,
      NewsDetails,
      Footer,
    },
    head(){
      return {
        title: "Potisen | News Details"
      }
    }
  }
</script>
