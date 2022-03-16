// ------------------------------------
// HTML

<template>
    
    <li class="card album">

        <figure class="card__thumb">
            <img :src="album.poster" alt="">
        </figure>

        <div class="card__info">
            <h3>{{ album.title }}</h3>
            <p>{{ album.author }}</p>
            <p>{{ album.year }}</p>
        </div>

    </li>

</template>

// ------------------------------------
// JS

<script>
    export default {
        props: {
            album: {
                type: Object,
                required: true,
            }
        }
    }
</script>

// ------------------------------------
// CSS

<style lang="scss" scoped>

.album {
    text-align: center;
    background-color: rgba(white, 0.07);
    padding: 10px;
}

</style>