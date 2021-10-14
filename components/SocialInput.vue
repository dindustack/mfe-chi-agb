<template>
<div>
    <!-- Input -->
    <label class="input-text mb-0">{{ label }}</label>
    <input type="text" placeholder="@" required />

</div>
</template>

<script>
export default {
    props: {
        label: {
            type: String,
            default: 'Label'
        }
    },
}
</script>

<style lang="scss">
.input-text {
    font-size: 14px;
    margin-top: 1rem;
    font-weight: 500;
    color: #141737;
}

input {
    width: 100%;
    font-size: 1rem;
    display: inline-block;
    box-sizing: border-box;
    padding: 12px 20px;
    margin: 8px 0;
    height: 2.5rem;
    border-radius: 5px;
    border: 1px solid #9fa4a8;

    @media only screen and (max-width: 568px) {
        width: 100%;

    }
}
</style>
