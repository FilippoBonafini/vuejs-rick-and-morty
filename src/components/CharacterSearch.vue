<script>
export default {
    name: 'Search'
}
</script>

<template>
    <div class="container">
        <form>
            <div class="row justify-content-center g-1">
                <div class="mb-3 col-12 col-sm-auto">
                    <label for="search-character" class="form-label d-none">Search Character</label>
                    <input type="text" class="form-control" id="search-character" aria-describedby="emailHelp"
                        placeholder="Search character">
                </div>
                <div class="mb-3 col-12 col-sm-auto">
                    <label for="search-status" class="form-label d-none">Password</label>
                    <select class="form-select" aria-label="Default select example" id="search-status">
                        <option selected>Select status</option>
                        <option value="1">One</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="mb-3 col-12 col-sm-auto">
                    <button type="submit" class="btn btn-primary me-1">Search</button>
                    <button type="reset" class="btn btn-secondary">Reset</button>
                </div>
            </div>
        </form>
    </div>
</template>


<style lang="scss" scoped></style>