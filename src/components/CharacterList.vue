<script>
import axios from 'axios';
import CharacterCard from './CharacterCard.vue';
import { store } from '../store';

export default {
    name: 'CharacterList',
    components: {
        CharacterCard
    },
    data() {
        return {
            store,

        }
    }
}
</script>

<template>
    <div class="container">
        <div class="row g-5">
            <div class="col-12 col-sm-3" v-for="character in store.characters">
                <CharacterCard :img="character.image" :name="character.name" :status="character.status"
                    :species="character.species" />
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped></style>