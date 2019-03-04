<template>
<div>




  <h3>f</h3>
  <h4>{{item.src}} </h4>
  

  

</div>
</template>
<script>
export default {
  name: 'ItemCard',
    props: {
    item: Object,
     required: true
    },computed: {
    classo:function(){
        return this.item.color1.filter(function(person){
           return person.alpha === "B"
        })
    },classP:function(){
        return this.item.color1.filter(function(person){
           return person.alpha === item.title.toString().charAt(0)
        })
    },filteredPeople: function() {
			var vm = this;
			var category = vm.item.selectedCategory;
			
			if(category === "All") {
				return vm.item;
			} else {
				return vm.item.src.filter(function(person) {
					return person.category === category;
				});
			}
		}

    },filters:{
         cut: item => {

      return item.charAt(0);

    }
    }
}
</script>