<script>
import { store } from "../store";
import AppButton from "../components/AppButton.vue";
import AppCardHome from "../components/AppCardHome.vue";
import AppProject from "../components/AppProject.vue";
import ContactForm from "../components/ContactForm.vue";
console.log(store);

export default {
  components: {
    AppButton,
    AppCardHome,
    AppProject,
    ContactForm,
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
        this.currentIndex =
          (this.currentIndex - 1 + this.store.projects.length) %
          this.store.projects.length;
      }
    },
  },
};
</script>

<template>
  <main class="container mt-5">
    <div class="jumbotron  border-0 bg-none">
      <div class="container py-5">
        <h1
          class="display-5 fw-bold element-text1"
          style="">
          Creazioni 3D: la soluzione per la visualizzazione realistica
        </h1>
        <ul class="d-flex g-3 mt-5 list_home" style="">
          <li class="me-3 element-text2"
            style="">
            <router-link :to="{ name: 'about' }" class="nav-link p-3"
              >Chi siamo</router-link>
          </li>
          <li
            class="me-3 element-text3"
            style="">
            <!-- <router-link :to="{ name: 'projects' }" class="nav-link p-3"
              >Progetti</router-link
            > -->
            <a href="#project">Progetti</a>
          </li>
          <li class="element-text4" style="">
            <router-link :to="{ name: 'contacts' }" class="nav-link p-3"
              >Contattaci</router-link
            >
          </li>
        </ul>
      </div>
    </div>
   
      <div class="container">
        <div class="row pt-5 row_card">
          <AppCardHome />
        </div>
      </div>
  
    <div class="content mb-5  pe-0 me-0 ms-0 pe-0 ps-0">
      <div class="container  pe-0 me-0 ms-0 pe-0 ps-0">
        <h3 style="color: #f15048; font-size: 3.2rem" class="pt-5 text-center fw-bold">
          Le nostre opere
        </h3>
        <p style="color: #f15048; font-size: 1.2rem" class="text-center mb-3">
          Il risultato del nostro processo di branding aziendale è una linea guida
          completa del marchio che può essere utilizzata per progettare un sito web di
          marketing e altre risorse di progettazione come le illustrazioni del marchio che
          riflettano il nuovo marchio .
        </p>
       
          <!-- Carosello -->
          <AppProject />
      
        
      </div>
    </div>

    <div class="container mt-5 mb-5" style="border-top: 4px solid #f15048">
      
        <!-- Colonna per il modulo -->
        <ContactForm />
      </div>
  
  </main>
</template>

<style lang="scss" scoped>

.element-text1 {
       max-width: min-content; 
       font-size: 5rem; 
       color: #f15048;
    }

    .list_home {
        list-style-type: none; 
        color: #f15048
    }

    .element-text2 {
        border-right: 4px solid white;
         padding-right: 30px; 
         font-size: 1.5rem
    }
    .element-text4 {
        font-size: 1.5rem
    }

    .element-text3 {
        border-right: 4px solid white; 
        padding-right: 30px; 
        font-size: 1.5rem
    }
    .jumbotron {
        padding: 3rem;
    }
    ul{
      display: flex;
      justify-content: start;
      align-items: center;
      padding-left: 0;

      li{
      a{
      text-decoration: none;
      color: #f15048
      }
    }
    }
    .nav-link {
      padding: 0  !important;
      padding-right: 14px !important;
    }
   

//   animazione ingresso scritta principale
@-webkit-keyframes bounce-in-right {
  0% {
    -webkit-transform: translateX(600px);
    transform: translateX(600px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
    opacity: 0;
  }
  38% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
    opacity: 1;
  }
  55% {
    -webkit-transform: translateX(68px);
    transform: translateX(68px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  72% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  81% {
    -webkit-transform: translateX(32px);
    transform: translateX(32px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  90% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  95% {
    -webkit-transform: translateX(8px);
    transform: translateX(8px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  100% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
}
@keyframes bounce-in-right {
  0% {
    -webkit-transform: translateX(600px);
    transform: translateX(600px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
    opacity: 0;
  }
  38% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
    opacity: 1;
  }
  55% {
    -webkit-transform: translateX(68px);
    transform: translateX(68px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  72% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  81% {
    -webkit-transform: translateX(32px);
    transform: translateX(32px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  90% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  95% {
    -webkit-transform: translateX(8px);
    transform: translateX(8px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  100% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
}

.element-text1 {
  -webkit-animation: bounce-in-right 1.5s both;
  animation: bounce-in-right 1.1s both; /* Per Safari e versioni più vecchie di Chrome */
}

.element-text2 {
  -webkit-animation: bounce-in-right 1.5s both;
  animation: bounce-in-right 1.3s both; /* Per Safari e versioni più vecchie di Chrome */
}

.element-text3 {
  -webkit-animation: bounce-in-right 1.5s both;
  animation: bounce-in-right 1.4s both; /* Per Safari e versioni più vecchie di Chrome */
}
.element-text4 {
  -webkit-animation: bounce-in-right 1.5s both;
  animation: bounce-in-right 1.5s both; /* Per Safari e versioni più vecchie di Chrome */
}

//carosello
.content {
      height: 130vh;
    }

.carousel {
  width: 100%;
  height: 100vh;
  position: relative;
  overflow: hidden;
}
@media (max-width: 768px) {
    .element-text1 {
        font-size: 2.5rem; 
        max-width: 100%; /* Imposta un valore percentuale corretto per max-width */
    }
    
    ul{
      display: flex;
      justify-content: center;
      align-items: center;

      li{
      a{
      text-decoration: none;
      color: #f15048
      }
    }
    }
    .list_home {
        font-size: 0.9rem;
    }
    .nav-link {
      padding: 0  !important;
      padding-right: 14px !important;
    }
    .element-text2 {
      
        padding: 0 !important;
        margin: 0;
         //padding-right: 15px; 
         font-size: 1rem
         
    }
    .element-text4{
        padding-right: 20px;
        margin-right: 20px;
        font-size: 1rem
    }

    .element-text3 {
        padding-right: 10px;
        font-size: 1rem
    }
    .router-link {
        padding: 0;
    }

    .jumbotron {
        padding: 0;
    }
}

@media (max-width: 768px) {
    .row_card {
        margin-left: 40px;
    }
    
   
}
@media (max-width: 768px) {
    .carousel {
        padding-bottom: 15px;
    }
    
    .content {
      height: 120vh;
    }
   
}



</style>
