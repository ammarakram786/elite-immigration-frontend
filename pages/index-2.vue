<template>
  <div>
    <NavTwo />
    <SliderTwo />
    <DonationForm />
    <CampaignTwo />
    <BrandsTwo />
    <AboutFive />
    <CallToActionThree />
    <TeamOne />
    <FunFactTwo />
    <VideoOne />
    <SubscribeOne />
    <ServiceOne />
    <TestimonialOne />
    <CallToActionOne />
    <Footer />
  </div>
</template>


<script>
  import NavTwo from "../components/NavTwo";
  import SliderTwo from "../components/SliderTwo";
  import DonationForm from "../components/DonationForm";
  import Footer from "../components/Footer";
  import CampaignTwo from "../components/CampaignTwo";
  import BrandsTwo from "../components/BrandsTwo";
  import AboutFive from "../components/AboutFive";
  import CallToActionThree from "../components/CallToActionThree";
  import TeamOne from "../components/TeamOne";
  import FunFactTwo from "../components/FunFactTwo";
  import VideoOne from "../components/VideoOne";
  import ServiceOne from "../components/ServiceOne";
  import TestimonialOne from "../components/TestimonialOne";
  import CallToActionOne from "../components/CallToActionOne";
  export default {
    components: {
      CallToActionOne,
      ServiceOne,
      TeamOne,
      CallToActionThree,
      CampaignTwo,
      NavTwo,
      SliderTwo,
      DonationForm,
      BrandsTwo,
      AboutFive,
      FunFactTwo,
      VideoOne,
      TestimonialOne,
      Footer,
    },
    head(){
      return {
        title: "Potisen | Home 2"
      }
    }
  }
</script>
