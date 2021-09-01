<script>
import { onMount } from "svelte";


	let number = []


	function addNumber(){
		number = [...number, number.length+1]
	}
	onMount(()=>{
		console.log("Wellcome to click count !!")
	})

	$: eff =  number.sort(function(a, b) {
  return a - b;
});
</script>

<main>
	<h2> COUNT : {eff.length}</h2>
	<h1>{eff.join(' ')}</h1>

	<div class="main_section">
		<button on:click={addNumber}>ClickMe!!</button>

	</div>
</main>

<style>
	h2{
		text-align: center;
	}
	h1{
		background-color: rgb(233, 240, 238);
		color: cornflowerblue;
		min-height: 8rem;
		max-height: 12rem;
		overflow-y: auto;
		margin: 0% 25%;
		word-wrap: break-word;
		text-align: center;
		align-items: center;
		padding: 20px  45px;
	}
	.main_section{
		margin: 4rem 0px;
	   text-align: center;
	}

	.main_section button{
		-webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
		background-color: cornsilk;
		border-radius: 10%;
		transition: cubic-bezier(0.075, 0.82, 0.165, 1);
		
	}
	.main_section  button:hover{
		box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.3);
		
	}
</style>