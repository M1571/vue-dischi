// -------------------------------
// HTML

<template>
    <main class="main">

        <section>
            <div class="container">
                <AlbumList /> 
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
}

</style>