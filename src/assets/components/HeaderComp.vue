<script>

export default {
  name: 'HeaderComp',
  props: ['titleProps']
}

</script>

<template>

    <header>

        <div class="header-container">

            <div class="my-2 d-flex justify-content-start align-items-center">
                
                <div class="logo-container">

                    <img src="public/img/b-logo.png" alt="">

                </div>

                <h1><mark>{{ titleProps }}</mark></h1>

            </div>

        </div>

    </header>

</template>

<style lang="scss" scoped>

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    .header-container {
        width: 80%;
        margin: 0 auto;
    }

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