<script lang="ts">

export default {
	name: "modal-organisation",
	methods:{

        handleClose(){
            this.$emit('closeEvent');
        }
    }
}
</script>

<template>

	<div class="modal">

		<div class="container">

			<slot name="photo"></slot>

			<div class="right">
				<div class="button" >
					<div class="bar" @click="handleClose"></div>
					<div class="bar" @click="handleClose"></div>
				</div>

				<div class="content">
					<h3><slot name="company-name"></slot></h3>

					<p>	<slot name="projet-description"></slot></p>

					<div class="technicalContainer">
						<div class="services element">
							<h4>Services proposés</h4>
							<ul>
								<li><slot name="service-one"></slot></li>
								<li><slot name="service-two"></slot></li>
								<li><slot name="service-three"></slot></li>
								<li><slot name="service-four"></slot></li>
							</ul>
						</div>

						<div class="langages element">
							<h4>Technologies utilisées</h4>
							<ul>
								<li><slot name="langages-one"></slot></li>
								<li><slot name="langages-two"></slot></li>
								<li><slot name="langages-three"></slot></li>
								<li><slot name="langages-four"></slot></li>
							</ul>
						</div>
					</div>
				</div>

				<div class="btnVisit">
					<slot name="websiteLink"></slot>
				</div>
				
			</div>
		</div>
	</div>
</template>

<style>
.modal{
	background-color: rgba(000, 000, 000, 0.5);
	position: fixed;
	height: 100vh;
	width: 100%;
	left: 0;
	top: 0;
	color: var(--blue);
	z-index: 999;
}

.modal .container{
	background: #fff;
    margin: auto;
    width: 85%;
    height: 85%;
    position: absolute;
    z-index: 9999;
	overflow: auto;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
	display: flex;
	flex-direction: row;
}

.modal .container .imageContainer{
	background-size: cover;
	flex: 1 1 50%;
	position: relative;
}

.modal .container .imageContainer img{
	width: 100%;
}

.modal .container .right{
	flex: 1 1 50%;
}

.modal .right .button{
	text-align: right;
	padding: 30px 20px;
}

.modal .right .button .bar{
	background-color: var(--blue);
	width: 30px;
	margin-left:auto;
	height: 1px;
	cursor: pointer;
}

.modal .right .button .bar:first-child{
	rotate: 45deg;
}

.modal .right .button .bar:last-child{
	rotate: -45deg;
}

.content{
	padding: 40px;
}

.content h3{
	font-size: 40px;
	font-family: var(--bold);
}

.content p{
	font-size: 20px;
	font-family: var(--light);
	padding: 30px 0;
	line-height: 150%;
}

.content .technicalContainer{
	display: flex;
	flex-direction: row;
}

.content .technicalContainer .element{
	flex: 1 1 50%
}

.content .technicalContainer .element h4{
	font-family: var(--bold);
	font-size: 20px;
	line-height: 150%;
}

.content .technicalContainer .element ul{
	font-family: var(--light);
	font-size: 16px;
	padding: 10px 20px;
	line-height: 150%;
}

.content .technicalContainer .element ul li{
	padding: 5px;
	list-style-type: none;
}


.btnVisit{
	text-align: center;
	padding: 20px;
}
.btnVisit a{
	text-align: center;
	text-decoration: none;
	background-color: var(--yellow);
	color: var(--white);
	font-size: 20px;
	font-family: var(--bold);
	padding: 10px 20px;
	border-radius: 5px;
	text-align: center;
	margin: auto;
}

@media screen and (max-width: 1200px)  {
	.content .technicalContainer{
		flex-direction: column;
	}

	.content h3{
		font-size: 30px;
	}

	.content p{
		font-size: 18px;
		padding: 20px 0;
	}

	.btnVisit a{
		font-size: 18px;
	}
}

@media screen and (max-width: 900px)  {

	.container{
		flex-flow: initial;
		flex-direction: column;
	}

	.container .imageContainer{
		height: 300px;
		flex: 1 1 100%;
	}
}


</style>