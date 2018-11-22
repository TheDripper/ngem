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
	</div>
	<div class="column is-one-quarter">

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

</style>
