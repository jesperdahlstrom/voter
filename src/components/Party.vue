<template>
    <div class="col">
        <img id="party-logo" v-bind:src="logo" style="height:90px">
        <p>{{name}}</p>
    </div>    
</template>

<script>
export default {
    name: 'Party',
    props: ['logo', 'name'],
}
</script>

<style scoped>
    #party-logo{
        cursor: pointer;
    }

</style>