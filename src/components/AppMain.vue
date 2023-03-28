<script>
import CharacterSearch from './CharacterSearch.vue';
import CharacterList from './CharacterList.vue';
export default {
    name: 'Main',
    components: {
        CharacterSearch,
        CharacterList
    },
    methods: {
        search() {
            console.log('Lancio un emit')
            this.$emit('search')
        },
        reset() {
            console.log('resetto i risultati')
            this.$emit('reset')
        }
    }
}
</script>

<template>
    <main>
        <CharacterSearch @search="search()" @reset=reset() />
        <CharacterList />
    </main>
</template>


<style lang="scss" scoped></style>