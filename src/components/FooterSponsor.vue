<script>
export default {
  props: {
    store: Object,
  },
  data() {
    return {};
  },
};
</script>

<template>
 <div class="container">
      <div class="scroller">
        <div v-for="curimage in store.sponsorArray" :key="curimage.id" class="scroller-item">
          <img :src="curimage.path" alt="" />
        </div>
        <div v-for="curimage in store.sponsorArray" :key="'duplicate-' + curimage.id" class="scroller-item">
          <img :src="curimage.path" alt="" />
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/_variables" as*;
.container {
  display: flex;
  overflow: hidden;
  width: 100%;
  max-width: 1700px; /* Set a maximum width for the container */
  -webkit-mask-image: linear-gradient(90deg, transparent 10%, #fff 40%, #fff 60%, transparent 90%);
  mask-image: linear-gradient(90deg, transparent 10%, #fff 40%, #fff 60%, transparent 90%);
}

img {
  font-size: 25px;
  text-transform: uppercase;
  font-weight: 500;
  letter-spacing: 1.5px;
  padding: 7px 15px;
  border-radius: 7px;
  box-shadow: rgba(255, 255, 255, 0.192) 0px 0px 15px;
}

.scroller {
  display: flex;
  gap: 50px; /* Increased space between images */
  animation: scroll 25s linear infinite;
}

.scroller-item {
  flex-shrink: 0;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-25%);
  }
}

</style>
