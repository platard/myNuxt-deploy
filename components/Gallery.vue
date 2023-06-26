<template>
    <div id="gallery" class="gallery">
        <div v-for="item in items" :key="item.id" 
        class="gallery-item">
            <img 
                :class="item.caught ? 'gallery-item-image caught' : 'gallery-item-image'"
                :src="`https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${item.id}.png`" 
                :alt="item.name"
                @click="toggleCaught(item)" />
            <NuxtLink :to="'/pokemon/' + item.id" >
                <h2 class="gallery-item-name"> {{ item.name }}</h2>
            </NuxtLink>
            <NuxtLink :to="`/pokemon/1`" >
                <h2 class="gallery-item-name"> pokemon</h2>
            </NuxtLink >
        </div>
    </div>
</template>

<script>
  export default {
    name: "Gallery",
    props: ['items'],
    methods: {
        toggleCaught: function(item) {
            this.$emit('toggle-caught', item)
            console.log(item.name)
        }
        }

  }
</script>