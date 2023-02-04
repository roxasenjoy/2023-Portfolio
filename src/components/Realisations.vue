<script lang="ts">

export default{
    data() {
        return { 
            ACDGC: 'ACDGC',
            TM: 'TM',
            ZESTE: 'ZESTE',
            LCDC: 'LCDC'
            
        }
    },
}

</script>

<template>
    
    <section>
        <div class="img-clip-block">
  			<div class="img-clip-block">
                <div class="img-clip-row">
                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap titleContainer">
                        <div class="overlay ">
                            <div class="overlay-content titleContent">Projets & Réalisations</div>
                        </div>
                    </a>

                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">			
                            <div class="overlay-content">{{ACDGC}}</div>
                        </div>
                    </a>
                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">			
                            <div class="overlay-content">{{TM}}</div>
                        </div>
                    </a>
                </div>
                

                <div class="img-clip-row">
                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">
                            <div class="overlay-content">{{ZESTE}}</div>
                        </div>
                    </a>

                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">			
                            <div class="overlay-content">{{LCDC}}</div>
                        </div>
                    </a>
                        
                </div>

                <div class="img-clip-row">
                    <!-- <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">
                            <div class="overlay-content">IMAGE</div>			
                        </div>
                    </a>

                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">			
                            <div class="overlay-content">IMAGE</div>
                        </div>
                    </a> -->

                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap containerDevis">
                        <div class="overlay devisOverlay">			
                            <div class="overlay-content devisContent">CRÉER VOTRE SITE INTERNET</div>
                        </div>
                    </a>
                        
                </div>

                <!-- <div class="img-clip-row">
                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">
                            <div class="overlay-content">IMAGE</div>			
                        </div>
                    </a>
                        
                </div>

                <div class="img-clip-row">

                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap">
                        <div class="overlay imageOverlay">			
                            <div class="overlay-content">IMAGE</div>
                        </div>
                    </a>

                    <a href="https://stocksnap.io/photo/J633WD7BAR" class="img-clip-wrap containerDevis">
                        <div class="overlay devisOverlay">			
                            <div class="overlay-content devisContent">CRÉER VOTRE SITE INTERNET</div>
                        </div>
                    </a>
                        
                </div> -->
            </div> <!-- /img-clip-block -->

        </div>
    
    </section>

</template>
  
<style scoped>

section{
    width: 100%;
    margin: 50vh 0 0 0;
    justify-content:space-between;
    flex-direction: row;
}


.clip-svg {
  width: 0;
  height: 0;
}

.img-clip-block {
  font-family: 'Cuprum', sans-serif;
  margin: 20px 0;
}

.img-clip-row {
  text-align: center;
  margin-top: -154px;
}

.img-clip-row:first-of-type .img-clip-wrap {
    background-position: top;
    margin: -30px 10px -30px 10px;

}

.img-clip-row:nth-of-type(2) .img-clip-wrap:nth-of-type(odd) {
    background-position: left;
    margin: 0 10px 0 0;
}

.img-clip-row:nth-of-type(2) .img-clip-wrap:nth-of-type(even) {
  background-position: right;
  margin: 0 0 0 10px;
}

.img-clip-row:last-of-type .img-clip-wrap {
  background-position: bottom;
  margin: -30px 10px -30px 10px;

}

.img-clip-wrap {
  width: 400px; 
  height: 400px; 
  position: relative;
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  -webkit-transition: all 0.4s ease-in;
  transition: all 0.4s ease-in;
  background-color: white;
  display: inline-block;
}

.overlay {
  /* background-color: none; */
  clip-path: polygon(50% 1%, 99% 50%, 50% 99%, 1% 50%);
  background-size: cover;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  pointer-events: none;
  -webkit-transition: all 0.3s linear;
  transition: all 0.3s linear;
}

.imageOverlay{
      background-image: url('@/assets/images/andrew.jpg');
}

.containerDevis{
    background-color: initial;
}
.devisOverlay{
    background-color: var(--yellow); 
}

.devisContent{
    font-family: var(--bold) !important;
    color: var(--white) !important;
}

.titleContainer .titleContent{
    color: var(--blue) !important;
}

.overlay-content {
    color: var(--white);
    text-transform: uppercase;
    position: absolute;
    left: 50%;
    top: 50%;
    -ms-transform: translateX(-50%) translateY(-50%);
    -webkit-transform: translateX(-50%) translateY(-50%);
    transform: translateX(-50%) translateY(-50%);
    text-shadow: 1px 1px 2px rgba(0,0,0,0.1);

    font-family: var(--normal);
    font-size: 26px;
}

.img-clip-wrap:hover {
  -webkit-transition: all 0.4s ease-in;
  transition: all 0.4s ease-in;
  transform: scale(1.1);
}

.img-clip-img {
  display: block;
}


/** Tablette **/
@media screen and (max-width: 1400px)  {

    
    section{
        margin: 40vh 0 0 0;
    }

    .img-clip-wrap {
        width: 300px; 
        height: 300px; 
    }
    .img-clip-row:nth-of-type(2) .img-clip-wrap:nth-of-type(odd) {
       margin: initial;
    }

    .img-clip-row:nth-of-type(2) .img-clip-wrap:nth-of-type(even) {
     margin: initial;
    }

    .img-clip-row:last-of-type .img-clip-wrap {
      margin: initial;
    }

    /* Première ligne */

    .img-clip-row:first-of-type .img-clip-wrap {
       margin: initial;
    }
    

    .img-clip-row{
        margin-top: -140px;
    }
}

/** Tablette **/
@media screen and (max-width: 918px)  {

    section{
        margin: 30vh 0 0 0;
    }
    .img-clip-row:first-of-type .img-clip-wrap {
       margin: 0 5px;
    }
    .img-clip-row:nth-child(1) .img-clip-wrap:last-child{
        margin-top: -145px;
    }

}

/** Tablette **/
@media screen and (max-width: 650px){

    section{
        margin: 25vh 0 0 0;
    }
    .img-clip-row{
        margin-top: 0px;
    }

    .img-clip-row:nth-child(1) .img-clip-wrap:last-child{
        margin-top: 0px;
    }
}

</style>
  