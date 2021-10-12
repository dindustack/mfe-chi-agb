<template>
    <div>
        <hr class="hr-solid" />
        <div class="button-container">
            <button class="bottom-button">{{ buttonText }}</button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        buttonText: {
            type: String,
            default: 'Button'
        }
    },
}
</script>

<style lang="scss">
.button-container {
  display: flex;
  justify-content: flex-end;
 
}

.bottom-button {
    background-color: #006AFF;
    border: 1px solid #006AFF;
    border-radius: 10px;
    color: #FFF;
    cursor: pointer;
    font-size: 14px;
    font-weight: bold;
    padding: 14px 23px;
    transition: all 0.2s ease-in-out;
    }
</style>