<template>
    <div class="row">
        <Party 
        v-for="party in parties"
        :logo="party.image"
        :name="party.name"
        :key="party.name">
        </Party>
    </div>    
</template>

<script>
import Party from './Party'

export default {
    name: 'PartyList',
    components: {
        Party
    },
    data () {
        return{
            parties: [
                {name: "Centerpartiet",
                image: require("../assets/partyLogos/c-logo.jpg")},
                {name: "Kristdemokraterna",
                image: require("../assets/partyLogos/kd-logo.jpg")},
                {name: "Liberalerna",
                image: require("../assets/partyLogos/l-logo.jpg")},
                {name: "Moderaterna",
                image: require("../assets/partyLogos/m-logo.jpg")},
                {name: "Miljöpartiet",
                image: require("../assets/partyLogos/mp-logo.jpg")},
                {name: "Socialdemokraterna",
                image: require("../assets/partyLogos/s-logo.jpg")},
                {name: "Sverigedemokraterna",
                image: require("../assets/partyLogos/sd-logo.jpg")},
                {name: "Vänsterpartiet",
                image: require("../assets/partyLogos/v-logo.jpg")}, 

            ]
        }
    }
}
</script>

<style scoped>

</style>