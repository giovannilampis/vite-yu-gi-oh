<script>

export default {
  name: 'HeaderComp',
  props: ['titleProps']
}

</script>

<template>

    <header>

        <div class="container">

            <div class="d-flex">
                
                <div class="logo-container">

                    <img src="public/img/b-logo.png" alt="">

                </div>

                <h1><mark>{{ titleProps }}</mark></h1>

            </div>

        </div>

    </header>

</template>

<style lang="scss" scoped>

    mark {
        background-color: rgb(200, 204, 228);
    }

    .logo-container {
        width: 4rem;
        aspect-ratio: 1 / 1;

    }

    img {
        width: 100%;
    }

</style>