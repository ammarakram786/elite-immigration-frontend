<template>
  <div>
    <NavTwo />
    <PageHeader title="News" />
    <News />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import PageHeader from "../components/PageHeader";
  import News from "../components/News";
  import Footer from "../components/Footer";
  export default {
    components: {
      NavTwo,
      PageHeader,
      News,
      Footer,
    },
    head(){
      return {
        title: "Potisen | News"
      }
    }
  }
</script>
