<template>
  <div class="flex w-72 gap-6 ml-[5%] items-center justify-center 
   h-18 rounded-xl  relative z-[9999]">
    <AudienceOverlay/>
    <FiftyOverlay/>
    <PhoneOverlay/>
  </div>
</template>

<style>
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 10;
}

</style>

<script>
import AudienceOverlay from '../icon/AudienceOverlay.vue';
import PhoneOverlay from '../icon/PhoneOverlay.vue'
import  FiftyOverlay from '../icon/FiftyOverlay.vue'

export default {
  name: 'LifeLine',
  components: {
    AudienceOverlay,
    FiftyOverlay,
    PhoneOverlay
  },
  data() {
    return {
      showBan:false
    };
  },
  methods: {
    showBanIcon() {
      // Reset all showBan values to false
      for (let key in this.showBan) {
        this.showBan[key] = false;
      }
      // Set the clicked icon's value to true
      this.showBan = true;
    }
  }
};
</script>
