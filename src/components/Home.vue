<template>
  <div class="home">
    <!--NavBar-->
    <div class="w3-top">
        <div class="topNav w3-bar w3-text-white expande-color w3-large">
            <a class="w3-bar-item w3-button">{{nombre}}</a>
            <a class="w3-bar-item w3-button w3-hide-small">Link 1</a>
            <a class="w3-bar-item w3-button w3-hide-small">Link 2</a>
            <a class="w3-bar-item w3-button w3-hide-small">Link 3</a>
            <a class="w3-bar-item w3-button w3-right w3-hide-large w3-hide-medium" @click.prevent="collapseNav">&#9776;</a>
        </div>

        <div id="mobnileNav" class="w3-bar-block w3-hide w3-hide-large w3-hide-medium w3-text-white expande-color w3-center">
            <a class="w3-bar-item w3-button">Link 1</a>
            <a class="w3-bar-item w3-button">Link 2</a>
            <a class="w3-bar-item w3-button">Link 3</a>
        </div>
    </div><!--END NavBar-->
    <!--Hero-->
    <div class="hero w3-display-container">
        <figure class=" logoFigure w3-display-middle w3-display-container">
            <img src="../assets/logo.png" alt="Expande Consejo Alumnos" class="w3-display-middle">
        </figure>
    </div><!--END Hero-->
    <!--InfoCircles-->
    <div class="infoCircles w3-row-padding expande-secondary">
        <div class="circle w3-center w3-col l3 m3 s6 w3-text-white">
            <div>
                <i class="fa fa-book w3-xxlarge circleIcon"></i>
                <p>Plan de Trabajo</p>
            </div>
        </div>
        <div class="circle w3-center w3-col l3 m3 s6 w3-text-white">
            <div>
                <i class="fa fa-info w3-xxlarge circleIcon"></i>
                <p>¿Quiénes somos?</p>
            </div>
        </div>
        <div class="circle w3-center w3-col l3 m3 s6 w3-text-white">
            <div>
                <i class="fa fa-group w3-xxlarge circleIcon"></i>
                <p>Repres y comisiones</p>
            </div>
        </div>
        <div class="circle w3-center w3-col l3 m3 s6 w3-text-white">
            <div>
                <i class="fa fa-lock w3-xxlarge circleIcon"></i>
                <p>Lockers</p>
            </div>
        </div>
    </div><!--END InfoCircles-->
    <!--council-->
    <div class="council w3-row-padding w3-content">
        <div class="councilRep w3-col l4 m4 s6 w3-center">
            <figure class="councilImg w3-badge w3-white">
                <img src="../assets/person-icon.png" alt="Person" class="w3-image">
            </figure>
            <p>Nombre</p>
            <p><i>Cargo</i></p>
        </div>
        <div class="councilRep w3-col l4 m4 s6 w3-center">
            <figure class="councilImg w3-badge w3-white">
                <img src="../assets/person-icon.png" alt="Person" class="w3-image">
            </figure>
            <p>Nombre</p>
            <p><i>Cargo</i></p>
        </div>
        <div class="councilRep w3-col l4 m4 s6 w3-center">
            <figure class="councilImg w3-badge w3-white">
                <img src="../assets/person-icon.png" alt="Person" class="w3-image">
            </figure>
            <p>Nombre</p>
            <p><i>Cargo</i></p>
        </div>
        <div class="councilRep w3-col l4 m4 s6 w3-center">
            <figure class="councilImg w3-badge w3-white">
                <img src="../assets/person-icon.png" alt="Person" class="w3-image">
            </figure>
            <p>Nombre</p>
            <p><i>Cargo</i></p>
        </div>
        <div class="councilRep w3-col l4 m4 s6 w3-center">
            <figure class="councilImg w3-badge w3-white">
                <img src="../assets/person-icon.png" alt="Person" class="w3-image">
            </figure>
            <p>Nombre</p>
            <p><i>Cargo</i></p>
        </div>
    </div><!--END council-->
    <!--contact-->
    <div class="contact expande-secondary w3-xxlarge w3-text-white">
        <p class="w3-center"><i class="fa fa-plus"></i> Contacto</p>
        <hr>
        <div class="media w3-content w3-padding">
            <p class="w3-large"><i class="fa fa-phone"> {{telefono}}</i></p>
            <p class="w3-large"><i class="fa fa-envelope"> {{mail}}</i></p>
        </div>
    </div><!--END contact-->
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      nombre: 'Expande Consejo',
      mail: 'expandeconsejo@gmail.com',
      telefono: '(+52) 1 1234 5678'
    }
  },
  methods : {
    collapseNav () {
        var x = document.getElementById("mobnileNav");
        if (x.className.indexOf("w3-show") == -1) {
            x.className += " w3-show";
        } else { 
            x.className = x.className.replace(" w3-show", "");
        }
    }
  }
}
</script>

<style scoped>
/*COLOR #9357A1 7860A7 F4E580*/
.expande-color {
    background-color: #9357A1 !important;
}
.expande-secondary {
    background-color: #7860A7 !important;
}
.home {
    height: 100%;
    width: 100%;
}
.hero {
    height: 400px;
    width: 100%;
    background: url('../assets/itam.jpg') no-repeat center fixed; 
    background-size: cover;
}
.logoFigure {
    height: 100%;
    width: 80%;
    margin: 0 auto 0;
    text-align: center;
}
.logoFigure img {
    max-height: 80%;
    max-width: 80%;
    margin-top: auto;
    margin-left: auto;
    margin-right: auto;
}
.infoCircles {
    width: 100%;
    padding-top: 10px;
    padding-bottom: 10px;
}
.circle {
    height: 80px;
    margin-bottom: 10px;
    padding-top: 5px;
    cursor: pointer;
}
.circle:hover {
    color: #9357A1 !important;
    background-color: white !important;
    border-radius: 10%;
}
.council {
    padding-top: 10px;
}
.councilImg {
    width: 95%;
    margin-left: auto;
    margin-right: auto;
    margin-top: 0;
    margin-bottom: 0;
}
/* Turn off parallax scrolling for tablets and phones. Increase/decrease the pixels if needed */
@media only screen and (max-device-width: 1024px) {
    .hero {
        background-attachment: scroll;
    }
}
</style>
