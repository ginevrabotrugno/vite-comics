<script>

export default {
    name: "AppCard",
    props: {
        details: Object
    }
}

</script>

<template>

    <div class="card">
        <div class="thumb">
            <img :src="details.thumb" :alt="details.series">
        </div>
        <h6> {{ details.series }} </h6>

    </div>


</template>

<style lang="scss" scoped>
    .card {
        width: calc((100% / 6) - 20px);
        cursor: pointer;
        margin-bottom: 50px;

        .thumb {
            width: 100%;
            aspect-ratio: 1/1;

                img {
                    width: 100%;
                    object-fit: cover;
                    height: 100%;
                    object-position: top;
                }                
            
            }

        h6 {
            color: #fff;
            margin-top: 15px;
            font-size: 15px;
        }
    }
</style>