<template>
<div class="columns cont">
	<div class="column is-three-quarters">
		<div class=slides>
			<div class="slide" v-for="slide in slides" :style="{ backgroundImage: 'url(' +slide.img+ ')' }" @mouseover="addFull">
				<div class=shade>
				<h5>{{ slide.head }}</h5>
				<p>{{ slide.text }}</p>
				</div>
			</div>
		</div>
		<div class="columns copy">
			<div class="column">
			<h2 class="home-h2-l">
			<a href="our-vision/">innovative</a>
			</h2>
			<p class="home-p">
			We believe that it's never too late to right a wrong, and that the restoration of the environment can be successfully achieved through a combination of science and will. 
			</p>
			<span class="home-more-span">[ <a href="our-vision/">more about our vision</a> ]</span>
			</div>

			<div class="column">
			<h2 class="home-h2-l">
			<a href="about-northgate">environmental</a>
			</h2>
			<p class="home-p">
			Northgate provides an uncommon level of personalized service and technical acumen on complex projects by embracing innovative and results-oriented environmental science and engineering.
			</p>
			<span class="home-more-span">[ <a href="about-northgate">more about Northgate</a> ]</span>
			</div>
			<div class="column">
			<h2 class="home-h2-l">
			<a href="what-we-do/">solutions</a>
			</h2>
			<p class="home-p">
			We specialize in interdisciplinary technical solutions. We move projects forward and help our clients achieve their objectives within budget, with solutions that are both practical and creative.
			</p>
			<span class="home-more-span">[ <a href="what-we-do/">more about what we do</a> ]</span>
			</div>
		</div>
	</div>
	<div class="column is-one-quarter">
		<h2 class="home-h2-r">
		<a href="news/">news</a>
		</h2>
		<p class="home-p">
		Have a few minutes? Check out our blog for periodic news and announcements.
		</p>
		<img class="home-pic-r margin-b" src="/typewriter.jpg" width="105" height="105">
		<h2 class="home-h2-r">
		<a href="about-northgate/working-with-northgate">certifications</a>
		</h2>
		<p class="home-p margin-b">
		Click here for a listing of our <a href="about-northgate/working-with-northgate">small and women-owned business certifications</a>.
		</p>
		<h2 class="home-h2-r">
		<a href="contact-northgate/">contact us</a>
		</h2>
		<img class="home-pic-r" src="/booth.jpg" width="105" height="105">
	</div>
</div>
  
</template>

<script>

export default {
	asyncData() {
		return {
			slides: [
				{
					img: '/slide-1.jpg',
					head: 'Innovative',
					text: 'While others walk, we prefer to climb.'
				},
				{
					img: '/slide-2.jpg',
					head: 'Perspective',
					text: 'Sometimes a fresh perspective makes all the difference.'
				},
				{
					img: '/slide-3.jpg',
					head: 'Focused',
					text: 'Every well-planned journey begins with a map.'
				},
				{
					img: '/slide-4.jpg',
					head: 'Responsive',
					text: 'Our solutions are tailored to fit the specific needs of each client'
				},
				{
					img: '/slide-5.jpg',
					head: 'Smart',
					text: 'We see the ecosystem, not just the forest or the trees.'
				}
			]
		}
	},
	methods: {
		addFull: function(e) {
			let big = e.target.closest('.slide')
			document.querySelectorAll('.slide').forEach(slide=>{
				slide.style.width="20%"
			})
			document.querySelectorAll('.shade').forEach(slide=>{
				slide.style.opacity='0'
			})
			big.style.width="50%"
			big.querySelector('.shade').style.opacity='1'
		}
	}
}
</script>

<style>
.shade {
	height: 80px;
	text-align: center;
	background: rgba(0,0,0,0.8);
	font-size: 13px;
	color: white;
	opacity: 0;
	transition: all 0.2s ease;
	width: 100%;
	padding: 10px;
	display: flex;
	flex-direction: column;
	justify-content: center;
}
.shade h5 {
	width: 100%;
	font-weight: bold;
}
.shade p {
	width: 100%;
}
.slides {
	display: flex;
	width: 100%;
}
.slide {
	height: 270px;
	background-size: cover;
	background-position: center;
	width: 20%;
	transition: width 0.15s linear;
	cursor: pointer;
	display: flex;
	flex-direction: column;
	justify-content: flex-end;
}
.full {
	width: 50%;
	flex-shrink: 0;
}
.home-h2-l {
	margin-top: 20px;
	margin-bottom: 15px;
}
.home-h2-r {
	margin-top: 15px;
	margin-bottom: 5px;
}
.home-h2-r:first-child {
	margin-top: 0;
}

</style>
