
<script>
export default {
    name:'AppSearch',

    data(){
        return{
            searchedString: '',
        }
    }

}
</script>
<template>
    <div>
        <input type="text" v-model="searchedString">
        <button @click="$emit('search',searchedString)">search</button>
    </div>
</template>
<style lang="scss" scoped>
    
</style>