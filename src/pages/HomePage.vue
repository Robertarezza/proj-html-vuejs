<script>
//import AppCardHome from '../components/AppCardHome.vue';
//import AppOtherProject from '../components/AppOtherProject.vue';
// import AppPackPrices from '../components/AppPackPrices.vue';
//import AppCitHomepage from '../components/AppCitHomepage.vue';
//import AppCardPackPrices from '../components/AppCardPackPrices.vue';
// import AppNewsBlog from '../components/AppNewsBlog.vue';
//import AppCarousel from '../components/AppCarousel.vue';
//import AppDoubleCard from '../components/AppDoubleCard.vue';
// import AppOurMissionSec from '../components/AppOurMissionSec.vue';
//import AppOtherProjectSection from '../components/AppOtherProjectSection.vue';
//import AppStylishSection from '../components/AppStylishSection.vue';
import { store } from '../store';
import AppButton from '../components/AppButton.vue'

export default {
    components: {
        //AppCardHome,
        //AppOtherProject,
        AppButton,
        // AppPackPrices,
        //AppCardPackPrices,
        //AppCitHomepage,
        // AppNewsBlog,
        //AppCarousel,
        //AppDoubleCard,
        // AppOurMissionSec,
        //AppOtherProjectSection,
        //AppStylishSection,
    },
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <main class="container-fluid">
     
        
<div class="jumbotron p-5 bg-light border-0 d-none">
    <div class="container py-5">

        <h1 class="display-5 fw-bold element-text1" style=" max-width: min-content; font-size: 5rem; color: #f15048">
            Creazioni 3D: la soluzione per la visualizzazione realistica
        </h1>
        <ul class="d-flex g-3 mt-5" style="list-style-type:none; color: #f15048">
            <li class="me-3 element-text2" style="border-right: 4px solid white; padding-right: 30px; font-size: 1.5rem">Chi siamo</li>
            <li class="me-3 element-text3" style="border-right: 4px solid white; padding-right: 30px; font-size: 1.5rem">Progetti</li>
            <li class="element-text4" style="font-size: 1.5rem">Articoli</li>
        </ul>
    </div>
</div>
<div class="content pb-5 d-none" style="background-color: #1b0c3b;">
    <div class="container">
        <div class="row pt-5">
            <div class="col-3">

                <div class="card  p-3 rounded element-class" style="">
                    <i class="fa-brands fa-unity text-shadow-pop-bottom  " style="font-size: xxx-large;"></i>
                    <p class="mt-4">Creazioni 3D</p>
                    <p style="text-align: center;">Creazioni 3D innovativa e accattivante.</p>
                </div>
            </div>
            <div class="col-3">
                <div class="card p-3 rounded element-class" style="">
                    <i class="fa-brands fa-unity text-shadow-pop-bottom  " style="font-size: xxx-large;"></i>
                    <p class="mt-4">Creazioni 3D</p>
                    <p style="text-align: center;">Creazioni 3D innovativa e accattivante.</p>
                </div>
            </div>
            <div class="col-3 ">
                <div class="card  p-3 rounded element-class" style="">
                    <i class="fa-brands fa-unity text-shadow-pop-bottom  " style="font-size: xxx-large;"></i>
                    <p class="mt-4">Creazioni 3D</p>
                    <p style="text-align: center;">Creazioni 3D innovativa e accattivante.</p>
                </div>
            </div>
            <div class="col-3">
                <div class="card   p-3 rounded element-class" style="">
                    <i class="fa-brands fa-unity text-shadow-pop-bottom  " style="font-size: xxx-large;"></i>
                    <p class="mt-4">Creazioni 3D</p>
                    <p style="text-align: center;">Creazioni 3D innovativa e accattivante.</p>
                </div>
            </div>
        </div>
    </div>
</div>
<div class="content" >
<div class="container d-none "  >

    <h3 style=" color: #f15048; font-size: 3.2rem;" class="pt-5 text-center fw-bold">Le nostre opere</h3>
    <p style=" color: #f15048; font-size: 1.2rem;" class="text-center mb-3">Il risultato del nostro processo di branding aziendale è una linea guida completa del marchio che può essere utilizzata per progettare un sito web di marketing e altre risorse di progettazione come le illustrazioni del marchio che riflettano il nuovo marchio .</p>
    <div class="row mt-5" id="card-container">
    <!-- Prima riga di card -->
    <div class="col-md-4 mb-4">
        <div class="card bg-image  " style="background-image: url('/img/spider.jpeg');">
            <!-- <div class="card-body">
                <h5 class="card-title">Card Title 1</h5>
                <p class="card-text">Descrizione della card numero 1.</p>
                <a href="#" class="btn btn-primary">Scopri di più</a>
            </div> -->
        </div>
    </div>
    <div class="col-md-4 mb-4">
        <div class="card bg-image" style="background-image: url('/img/spider.jpeg');">
            <!-- <div class="card-body">
                <h5 class="card-title">Card Title 2</h5>
                <p class="card-text">Descrizione della card numero 2.</p>
                <a href="#" class="btn btn-primary">Scopri di più</a>
            </div> -->
        </div>
    </div>
    <div class="col-md-4 mb-4">
        <div class="card bg-image" style="background-image: url('/img/spider.jpeg');">
            <!-- <div class="card-body">
                <h5 class="card-title">Card Title 3</h5>
                <p class="card-text">Descrizione della card numero 3.</p>
                <a href="#" class="btn btn-primary">Scopri di più</a>
            </div> -->
        </div>
    </div>
    <!-- Seconda riga di card -->
    <div class="col-md-4 mb-4">
        <div class="card bg-image" style="background-image: url('/img/spider.jpeg');">
            <!-- <div class="card-body">
                <h5 class="card-title">Card Title 4</h5>
                <p class="card-text">Descrizione della card numero 4.</p>
                <a href="#" class="btn btn-primary">Scopri di più</a>
            </div> -->
        </div>
    </div>
    <div class="col-md-4 mb-4">
        <div class="card bg-image" style="background-image: url('/img/spider.jpeg');">
            <!-- <div class="card-body">
                <h5 class="card-title">Card Title 5</h5>
                <p class="card-text">Descrizione della card numero 5.</p>
                <a href="#" class="btn btn-primary">Scopri di più</a>
            </div> -->
        </div>
    </div>
    <div class="col-md-4 mb-4">
        <div class="card bg-image" style="background-image: url('/img/spider.jpeg');">
            <!-- <div class="card-body">
                <h5 class="card-title">Card Title 6</h5>
                <p class="card-text">Descrizione della card numero 6.</p>
                <a href="#" class="btn btn-primary">Scopri di più</a>
            </div> -->
        </div>
    </div>
</div>


</div>
</div>
           
    
    </main>
</template>

<style lang="scss" scoped>
main {
    padding-top: 80px;
}




</style>