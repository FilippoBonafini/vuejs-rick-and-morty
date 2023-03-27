<script>
import { store } from '../store';
export default {
    name: 'Footer',
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <footer class="text-center my-5">
        Risultati trovati:{{ store.charactersFound }}
    </footer>
</template>


<style lang="scss" scoped></style>