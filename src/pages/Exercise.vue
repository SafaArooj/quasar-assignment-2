<template>
	<!--
	Awesome Exercise 2 - Vue.js Lists & Components

1) Create an array for the food items you see on the page. Each object in the array should contain properties for the image url, name, description and deliciousness
2) Create a v-for loop that displays these food items onto the page, with all the data coming from the food array (hint: for the image src, use :src)
3) Add your own food item to the list
4) Create a child component and use it to display each of your items (don't use the components/Solution/Food.vue file)
5) Add unique id's to the food array for each item, and apply these to a :key property on your v-for loop

	-->
  <q-page padding>
  	<div class="q-pa-md row items-stretch">

	<ul style="display: grid;grid-template-columns:auto auto auto">
		<!-- <li v-for="(food) in foods" :key="food.id">
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
		</li> -->

		<food v-for="(food) in foods" :key="food.id" :food="food"></food>
	</ul>	
  	  
  	</div>
  </q-page>
</template>

<script>
import Food from '../components/Solution/Food.vue'
	export default {
		data() {
			return {
				foods: [
					{
					id: 1,
					name: 'Burger',
					image: 'https://i.imgur.com/0umadnY.jpg',
					desc: 'A burger is a sandwich consisting of one or more cooked patties of ground meat, usually beef, placed inside a sliced bread roll or bun.',
					delicousness: 3
					},
					{
					id: 2,
					name: 'Pizza',
					image: 'https://i.imgur.com/b9zDbyb.jpg',
					desc: 'Pizza is a savory dish of Italian origin, consisting of a usually round, flattened base of leavened wheat-based dough.',
					delicousness: 3
					},
					{
					id: 3,
					name: 'Sprouts',
					image: 'https://i.imgur.com/RbKjUjB.jpg',
					desc: 'The Brussels sprout is a member of the Gemmifera Group of cabbages, grown for its edible buds.',
					delicousness: 1
					},
					{
					id: 4,
					name: 'Biryani',
					image: 'https://i.imgur.com/5MD6WEJ.jpeg',
					desc: 'Biryani is a mixed rice dish originating among the Muslims of the Indian subcontinent',
					delicousness: 5
					},
					
				]
			}
		},
		components: {
			'food': require('components/Food.vue').default
		}
	}
</script>

<style>
</style>
