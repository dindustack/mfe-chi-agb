<template>
<div class="left-side-image">
    <div class="image-container">
        <!-- <img src="~/assets/image/cover.png"  alt="cover"> -->
    </div>
</div>
</template>

<script>

</script>

<style lang="scss">
.left-side-image {
    position: relative;
    top: 0;
    background-color: #0262D2;
    display: none;

    @media (min-width: 992px) {
        display: block !important;
    }

    .image-container {
        vertical-align: bottom;
        display: table-cell;
    }

}
</style>
