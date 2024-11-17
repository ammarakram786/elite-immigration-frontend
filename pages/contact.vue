<template>
  <div>
    <NavTwo />
    <PageHeader title="Contact" />
    <Contact />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import PageHeader from "../components/PageHeader";
  import Contact from "../components/Contact";
  import Footer from "../components/Footer";
  export default {
    components: {
      NavTwo,
      PageHeader,
      Contact,
      Footer,
    },
    head(){
      return {
        title: "Potisen | Contact"
      }
    }
  }
</script>
