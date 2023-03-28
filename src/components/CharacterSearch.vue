<script>
import { store } from '../store';
export default {
    name: 'Search',
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container">
        <form @submit.prevent="$emit('search')">
            <div class="row justify-content-center g-1">
                <div class="mb-3 col-12 col-sm-auto">
                    <label for="search-character" class="form-label d-none">Search Character</label>
                    <input type="text" class="form-control" id="search-character" aria-describedby="emailHelp"
                        placeholder="Search character" v-model="store.searchKey">
                </div>
                <div class="mb-3 col-12 col-sm-auto">
                    <label for="search-status" class="form-label d-none">Select Stauts</label>
                    <select class="form-select" aria-label="Default select example" id="search-status"
                        v-model="store.searchStatus">
                        <option selected value="">Select status</option>
                        <option value="alive">Alive</option>
                        <option value="dead">Dead</option>
                        <option value="unknow">Unknow</option>
                    </select>
                </div>
                <div class="mb-3 col-12 col-sm-auto">
                    <button type="submit" class="btn btn-primary me-1">Search</button>
                    <button type="reset" class="btn btn-secondary" @click="$emit('reset')">Reset</button>
                </div>
            </div>
        </form>
    </div>
</template>


<style lang="scss" scoped></style>