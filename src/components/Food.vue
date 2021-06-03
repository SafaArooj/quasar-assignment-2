<template>
	<li style="width: 100%;display: inline">
			<div class="card shadow-1">
				<img :src= "food.image" width="198" height="180">
				<h1 class="text-primary">{{ food.name }}</h1>
				<p>{{ food.desc }}</p>
				<p>
	  	  		<small>
	  	  			<b>Delicousness:</b>
	  	  		</small>
	  	  		<b class="text-primary">
		  	  		{{ food.delicousness }}/5
	  	  		</b>
  	  			</p>
			</div>
		</li>
</template>

<script>
    export default {
        props: ['food']
    }
</script>

<style>
    .card {
		flex-basis: 210px;
		border: 1px solid #ccc;
		border-radius: 5px;
		padding: 5px;
		margin-right: 10px;
		margin-bottom: 10px;
	}
	.card img {
		max-width: 100%;
	}
	.card-content {
		padding: 0 10px;
	}
	h1 {
		font-size: 23px;
	}
	p {
		font-size: 14px;
	}
</style>



