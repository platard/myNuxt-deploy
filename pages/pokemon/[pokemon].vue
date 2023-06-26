<!-- <script setup>
const route = useRoute()

// When accessing /posts/1, route.params.id will be 1
console.log(route.params.pokemon)
</script>

<template>
    <h2>Pokemon</h2>
    <p>Id: {{ item.id }}</p>
    <p>Name: {{ item.name }}</p>
    <p>Caught: {{ item.caught }}</p>
    <img 
        :class="item.caught ? 'gallery-item-image caught' : 'gallery-item-image'"
        :src="`https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${route.params.pokemon}.png`" 
        :alt="item.name"/>

    <form @submit.prevent="updateItem">
        <input v-model="item.name" type="text" placeholder="Name"><br/>
        <button type="submit">Update Name</button>
    </form>
</template>

<script>
export default {
    name: 'Pokemon',
    data: function(){
        return {
            item: { },
            items: [],
            
        }
    },
    created() {
        // const storedItems = localStorage.getItem('items');
        const storedItems = [
    { id: 1, name: 'bulbasaur', caught: false },
    { id: 2, name: 'ivysaur', caught: false },
    { id: 3, name: 'venusaur', caught: false},]
        // if (storedItems) {
        //     this.items = JSON.parse(storedItems)
        //     this.item = JSON.parse(storedItems).find(item => item.id == this.route.params.pokemon )
        // }
        this.items = storedItems
        this.item = storedItems[0]
    },
    methods: {
      updateItem() {
        localStorage.setItem('items',  JSON.stringify(this.items.map( item => item.id == this.item.id ? {...this.item} : item ) ) )

        this.$router.push('/')

      },
    }
}
</script> -->


<template>
    <div>
        <h1>This is a slug</h1>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>