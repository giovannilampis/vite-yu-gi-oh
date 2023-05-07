<script>
export default {
    name: 'FindCharacter'
}

</script>

<template>

    <form class="form-inline row">

        <div class="col-12 col-md-4">
            <label class="sr-only" for="inlineFormInputName2">Name</label>
            <input type="text" class="form-control mb-2 mr-sm-2" id="inlineFormInputName2" placeholder="Search a card">
        </div>

        <div class="col-12 col-md-4">
            <label class="sr-only" for="card-name">Card Name</label>
            <div class="input-group mb-2 mr-sm-2">
                <input type="text" class="form-control" id="card-name" placeholder="Username">
            </div>
        </div>

        <div class="col-12 col-md-4">
             <button type="submit" class="btn btn-primary mb-2">Submit</button>
        </div>

    </form>

</template>

<style lang="scss" scoped>


</style>