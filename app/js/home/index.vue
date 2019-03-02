<template lang="html">
    <div>
       <Heador></Heador>
       <Hslider></Hslider> 
       <Novice></Novice>
    </div>
</template>

<script>
import Heador from "../public/header.vue";
import Hslider from "./hslider.vue";
import Novice from "./novice.vue";
export default {
  components: {
    Heador,
    Hslider,
    Novice
  }
};
</script>

