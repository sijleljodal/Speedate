	  <script>
      import { slide } from 'svelte/transition'
      export let name
      </script>
      
      <div class='happening' in:slide out:slide>
		 <h2>Its happening!{name}</h2>
	  </div>


      <style>

      	.happening{
		position:fixed;
		top:3rem;
		right:3rem;
		padding:2rem;
		background: #fec1eb;
		color: #ff00ae;
	}
      </style>