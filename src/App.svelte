
<script>

let side1Bobble1 = false
let flaske 

let side1 = false

const animateFlaske = () => {
	console.log('animate', flaske)
	flaske.src='./flaskeanim.gif'
}

let startShow = false
</script>


<main>
<section class='doors'>
<img on:click={()=> side1=!side1} src='https://i.pinimg.com/originals/b0/f3/60/b0f36062c5eef964aab385b4fc60104d.png' alt='tre1'>

<img src='https://i.pinimg.com/originals/b0/f3/60/b0f36062c5eef964aab385b4fc60104d.png' alt='tre1'>
</section>

<section class='dates'>
<section class="side1">
	<img on:click={() => side1Bobble1 = !side1Bobble1} 
	src='https://images.fineartamerica.com/images/artworkimages/mediumlarge/1/old-man-greg-joens.jpg' alt='bilde'>
	
	{#if side1Bobble1}
		<img 
		class='snakkeboble' 
		src='https://images.twinkl.co.uk/tr/image/upload/illustation/How-Pink-Speech-Bubble--Icon-Cartoon-Comic-MPS-KS2-bw-RGB.png'
		style='position: absolute;top:10rem; left:60%;' 
		alt='snak'>
	{/if}
	<img 
		on:click={animateFlaske}
		bind:this={flaske}  
		src= './flaske.png'
		style='
		position: absolute;
		top: 20vh;
		left: 20vh;
		'
		alt='pissss'
	>

</section>

<section class="side2">2</section>
<section class="side3">3</section>

</section>
</main>



<style>


main{
margin: 0;
padding: 0;
}

section{
	width: 100vw;
	height: 100vh;
	scroll-snap-align: start;
	scroll-snap-stop: always;
	display: grid;
	place-items: center;
	position: relative;
}

.doors{
	width: 100vw;
	display: grid;
	grid-auto-flow: column;
}

.dates{
	height: 100vh;
	display: grid;
	grid-auto-flow: column;
	overflow: scroll;
	scroll-snap-type: x mandatory;
}

section img{
	width: 30vw;
}

section:nth-of-type(even){
	background-color: antiquewhite;
} 
:global(html, body){
	margin: 0;
	padding: 0;
}
</style>