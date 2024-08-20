<script>
import { store } from "../store";
import AppButton from "../components/AppButton.vue";
import AppCardHome from "../components/AppCardHome.vue";
console.log(store);

export default {
  components: {
    AppButton,
    AppCardHome,
  },
  data() {
    return {
      store,
      currentIndex: 0,
    };
  },
  computed: {},
  methods: {
    nextImage() {
    if (this.store.projects.length) {
      this.currentIndex = (this.currentIndex + 1) % this.store.projects.length;
    }
  },
  prevImage() {
    if (this.store.projects.length) {
      this.currentIndex = (this.currentIndex - 1 + this.store.projects.length) % this.store.projects.length;
    }
  }
}
};
</script>

<template>
      <div class="list bg-none" >
   <div v-for="(project, index) in store.projects" :key="index" class="item" :class="{ active:            currentIndex === index, previous: (currentIndex - 1 + store.projects.length) % store.projects.length === index, next: (currentIndex + 1) % store.projects.length === index }">
              <img :src="project.img" alt="Carosello Immagine"  class=""/>
              <div class="content ">
                <h2 class="title">{{ project.title }}</h2>
                <p class="text">{{ project.text }}</p>
              </div>
            </div>
        </div>
<!-- Controlli del Carosello -->
        <div class="arrows mb-5">
            <i class="fa-solid fa-circle-arrow-left prev"  @click="prevImage"></i>
           <i class="fa-solid fa-circle-arrow-right next" @click="nextImage"></i>
          </div>
</template>

<style lang="scss" scoped >


.item.previous {
  left: 10%;
  opacity: 0.8;
  transform: scale(0.5);
  z-index: 1;
  height: 50%;
}

.item.next {
  right: 10%;
  opacity: 0.5;
  transform: scale(0.5);
  z-index: 1;
}

.item img {
 max-width: 100%;
  object-fit: cover;
}

.list {
  position: relative;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}


.arrows {
 // position: absolute;
  //top: 50%;
  width: 100%;
  display: flex;
  justify-content: center;
  transform: translateY(-100%);
}

.arrows i {
  background-color: #f15048;
  border: none;
  //padding: 10px 5px;
  text-align: center;
  cursor: pointer;
  font-size: 2rem;
  color: white;
  border-radius: 50%;
  outline: none;
  margin-left: 10px;
}

.item {
position: absolute;
width: 300px;
height: 400px;
transition: all 3s cubic-bezier(0, 0, 0.2, 1);
transform: translateX(100px);
opacity: 0;
// transform: scale(0.8);
}

@media (max-width: 768px) {

.list {
    padding-bottom: 90px;
}

.arrows{
    margin-top: 10px;
}

.item.previous {
left: 35%;
opacity: 2;
transform: scale(0.3);
z-index: 1;
height: 50%;
}

.item.next {
right: 35%;
opacity: 2;
transform: scale(0.3);
z-index: 1;
}

}


.item.active {
opacity: 1;
transform: scale(1);
z-index: 2;

.text  {
color: #f15048;
}

.title {
color: #f15048;
}
}

</style>