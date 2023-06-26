<template>
  <div>
    <h1>Welcome to the homepage</h1>
    <AppAlert>
      This is an auto-imported component.
    </AppAlert>

    <NuxtLink :to="`/pokemon/${id}`" >
                <h2 class="gallery-item-name"> pokemon</h2>
            </NuxtLink >
  </div>
  <NuxtPage />
</template>

<script>

export default {
  data: function() {
    return {
      id: 3
    }
  }
}
</script>

<style>
h1{
  color: red;
}
</style>
