<script>
export default {
    name: 'AppMovie',

    props:{
        movies:{
            type:Array,
            required:true
        }
    }
}
</script>
<template>
    <div>
      <article v-for="movie in movies">{{ movie.title }}</article>
    </div>
</template>
<style lang="scss" scoped>
    
</style>