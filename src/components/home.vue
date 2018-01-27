<template>
  <div>
    <landing-section-1></landing-section-1>
    <landing-section-2></landing-section-2>
    <landing-section-3></landing-section-3>
    <landing-section-4></landing-section-4>
    <landing-section-5></landing-section-5>
    <landing-section-6></landing-section-6>
    <landing-section-7></landing-section-7>
  </div>
</template>

<script>
import LandingSection1 from './landing/LandingSection1';
import LandingSection2 from './landing/LandingSection2';
import LandingSection3 from './landing/LandingSection3';
import LandingSection4 from './landing/LandingSection4';
import LandingSection5 from './landing/LandingSection5';
import LandingSection6 from './landing/LandingSection6';
import LandingSection7 from './landing/LandingSection7';
export default {
  name: 'Home',
  components: {
    LandingSection1,
    LandingSection2,
    LandingSection3,
    LandingSection4,
    LandingSection5,
    LandingSection6,
    LandingSection7
  },
  data() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
