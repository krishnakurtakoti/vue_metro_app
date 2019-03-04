<template>
<div>




  <h3>m</h3>
 

<h5 v-for="group in person1.liststation">{{group.alpha}} </h5>
  
<ul class="people-list">
		<li v-for="x in filteredPeople2">{{ x.liststation.length }}</li>
	</ul>
  

</div>
</template>
<script>
export default {
  name: 'DisplayEndResults',
    props: {
    person1: Object,
     required: true
    },data() {
    return {
selectedCategory:"All",selectedCategory1:"All"
    }
    },
    computed: {
      filteredPeople2: function() {
			var vm = this;
			var category1 = vm.selectedCategory1;
			var category = vm.selectedCategory;
			if(category1 === "All") {
				return person1;
			} else {
				return vm.person1.filter(function(person) {
					return person.dst === category1 && person.src === category;
				});
			}
		}
    

    }
}
</script>