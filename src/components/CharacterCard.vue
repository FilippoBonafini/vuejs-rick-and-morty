<script>
export default {
    name: 'CharacterCard',
    props: {
        img: String,
        name: String,
        status: String,
        species: String
    }
}
</script>

<template>
    <article class="text-center">
        <div class="img">
            <img class="rounded-circle img-fluid" :src="img" alt="">
        </div>
        <h3>{{ name }}</h3>
        <div>{{ status }}</div>
        <div>{{ species }}</div>
    </article>
</template>


<style lang="scss" scoped></style>