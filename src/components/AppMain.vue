<script>
import CharacterSearch from './CharacterSearch.vue';
import CharacterList from './CharacterList.vue';
export default {
    name: 'Main',
    components: {
        CharacterSearch,
        CharacterList
    }
}
</script>

<template>
    <main>
        <CharacterSearch />
        <CharacterList />
    </main>
</template>


<style lang="scss" scoped></style>