<script lang="ts">

import modalOrganisation from "@/components/templates/modal-organisation.vue";

export default{
	components: {modalOrganisation},
    data() {
        return { 
            ACDGC: 'ACDGC',
            TM: 'TM',
            ZESTE: 'ZESTE',
            LCDC: 'LCDC',
            modal: 0
            
        }
    },

    methods:{
		closeModal(){
			this.modal = 0;
		}
	}
}


</script>

<template>

    <div>
		<div class="container">
			<transition name="modalOrganisation">
				<div class="modal-mask">
					<modalOrganisation @closeEvent="closeModal" v-if="modal==1">
                        <template #photo>
                            <div class="imageContainer ACDGCBackground">
                                <div class="imageContainer ACDGCBackground"></div>
                            </div>	
                        </template>

                        <template #company-name>Zeste, la cuisine du jardin</template>
                        <template #projet-description>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit 
                            elementum lacinia. Donec quis molestie nibh. Interdum et malesuada 
                            fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna,
                            sed blandit sem facilisis non. Curabitur libero velit, dignissim eu 
                        </template>

                        <template #service-one>1</template>
                        <template #service-two>2</template>
                        <template #service-three>3</template>
                        <template #service-four>4</template>

                        <template #langages-one>5</template>
                        <template #langages-two>6</template>
                        <template #langages-three>7</template>
                        <template #langages-four>8</template>

                        <template #websiteLink>
                            <a href="http://zeste.andrewmahe.com/" target="_blank">Visiter le site</a>
                        </template>
                    </modalOrganisation>
				</div>
			</transition>

            <transition name="modalOrganisation">
				<div class="modal-mask" v-if="modal==2">
					<modalOrganisation @closeEvent="closeModal">
                        <template #photo>
                            <div class="imageContainer zesteBackground">
                                <div class="imageContainer zesteBackground"></div>
                            </div>	
                        </template>

                        <template #company-name>Zeste, la cuisine du jardin</template>
                        <template #projet-description>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit 
                            elementum lacinia. Donec quis molestie nibh. Interdum et malesuada 
                            fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna,
                            sed blandit sem facilisis non. Curabitur libero velit, dignissim eu 
                        </template>

                        <template #service-one>1</template>
                        <template #service-two>2</template>
                        <template #service-three>3</template>
                        <template #service-four>4</template>

                        <template #langages-one>5</template>
                        <template #langages-two>6</template>
                        <template #langages-three>7</template>
                        <template #langages-four>8</template>

                        <template #websiteLink>
                            <a href="http://zeste.andrewmahe.com/" target="_blank">Visiter le site</a>
                        </template>
                    </modalOrganisation>
				</div>
			</transition>

            <transition name="modalOrganisation">
				<div class="modal-mask" v-if="modal==3">
					<modalOrganisation @closeEvent="closeModal">
                        <template #photo>
                            <div class="imageContainer zesteBackground">
                                <div class="imageContainer zesteBackground"></div>
                            </div>	
                        </template>

                        <template #company-name>Zeste, la cuisine du jardin</template>
                        <template #projet-description>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit 
                            elementum lacinia. Donec quis molestie nibh. Interdum et malesuada 
                            fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna,
                            sed blandit sem facilisis non. Curabitur libero velit, dignissim eu 
                        </template>

                        <template #service-one>1</template>
                        <template #service-two>2</template>
                        <template #service-three>3</template>
                        <template #service-four>4</template>

                        <template #langages-one>5</template>
                        <template #langages-two>6</template>
                        <template #langages-three>7</template>
                        <template #langages-four>8</template>

                        <template #websiteLink>
                            <a href="http://zeste.andrewmahe.com/" target="_blank">Visiter le site</a>
                        </template>
                    </modalOrganisation>
				</div>
			</transition>

            <transition name="modalOrganisation">
				<div class="modal-mask" v-if="modal == 4">
					<modalOrganisation @closeEvent="closeModal">
                        <template #photo>
                            <div class="imageContainer LCDCBackground">
                                <div class="imageContainer LCDCBackground"></div>
                            </div>	
                        </template>

                        <template #company-name>Zeste, la cuisine du jardin</template>
                        <template #projet-description>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit 
                            elementum lacinia. Donec quis molestie nibh. Interdum et malesuada 
                            fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna,
                            sed blandit sem facilisis non. Curabitur libero velit, dignissim eu 
                        </template>

                        <template #service-one>1</template>
                        <template #service-two>2</template>
                        <template #service-three>3</template>
                        <template #service-four>4</template>

                        <template #langages-one>5</template>
                        <template #langages-two>6</template>
                        <template #langages-three>7</template>
                        <template #langages-four>8</template>

                        <template #websiteLink>
                            <a href="http://zeste.andrewmahe.com/" target="_blank">Visiter le site</a>
                        </template>
                    </modalOrganisation>
				</div>
			</transition>
		</div>
	</div>

    <section>
        <div class="img-clip-block">
  			<div class="img-clip-block">
                <div class="img-clip-row">
                    <a class="img-clip-wrap titleContainer">
                        <div class="overlay overlayContainer">
                            <div class="overlay-content titleContent">Projets & Réalisations</div>
                        </div>
                    </a>

                    <a class="img-clip-wrap" @click="modal=1">
                        <div class="overlay imageOverlay" :class="ACDGC">			
                        </div>
                    </a>
                    <a class="img-clip-wrap" @click="modal=2">
                        <div class="overlay imageOverlay" :class="TM">			
                        </div>
                    </a>
                </div>
                

                <div class="img-clip-row">
                    <a class="img-clip-wrap" @click="modal=3">
                        <div class="overlay imageOverlay" :class="ZESTE"></div>
                    </a>

                    <a class="img-clip-wrap" @click="modal=4"> 
                        <div class="overlay imageOverlay" :class="LCDC">			
                            <!-- <div class="overlay-content">{{LCDC}}</div> -->
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

                    <a href="#" class="img-clip-wrap containerDevis">
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


.zesteBackground{
    background-image: url('@/assets/images/portfolio/zeste.png');
}

.LCDCBackground{
    background-image: url('@/assets/images/portfolio/LCDC.png');
}

.ACDGCBackground{
    background-image: url('@/assets/images/portfolio/ACDGC.png');
}

.TMBackground{
    background-image: url('@/assets/images/portfolio/zeste.png');
}

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

.LCDC{
    background-image: url('@/assets/images/logo/LCDC.jpg');
}

.ZESTE{
    background-image: url('@/assets/images/logo/zeste.png');
}

.TM{
    background-image: url('@/assets/images/andrew.jpg');
}

.ACDGC{
    background-image: url('@/assets/images/logo/ACDGC.png');
}

.titleContainer,
.containerDevis{
    background-color: initial;
}
.titleContainer::after,
.containerDevis::after {
  aspect-ratio: 1;
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 400px;
  height: 400px;
  clip-path: polygon(100.00% 50.00%,50.00% 100.00%,0.00% 50.00%,50.00% 0.00%,100.00% 50.00%,calc(50.00% - -0.00px) calc(0.00% - -2.00px),calc(0.00% - -2.00px) calc(50.00% - 0.00px),calc(50.00% - 0.00px) calc(100.00% - 2.00px),calc(100.00% - 2.00px) calc(50.00% - 0.00px),calc(50.00% - -0.00px) calc(0.00% - -2.00px));
}

.titleContainer::after{
    background-color: var(--white);
}
.containerDevis::after {
    background-color:var(--yellow);
}

.devisContent{
    color: var(--yellow) !important;
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

    .titleContainer::after,
    .containerDevis::after {
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
  