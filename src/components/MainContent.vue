// -------------------------------
// HTML

<template>
    <main class="main">

        <section>
            <input class="input-search" type="search" name="" id="">
        </section>

        <section>
            <div class="container">
                <AlbumList class="listt" /> 
            </div>
        </section>

    </main>
</template>

// -------------------------------
// JS

<script>
import AlbumList from './AlbumList.vue'

    export default {
        components: {
            AlbumList,
        }
    }
</script>

// -------------------------------
// CSS

<style lang="scss" scoped>

.main {
    background-color: #1E2D3B;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 100px 40px;
    gap: 80px;
}

.input-search {
    padding: 5px 80px;
    box-shadow: 0px 0px 10px #1AD760;
    border: none;
    border-radius: 5px;
}

.listt {
    cursor: pointer;
}

</style>