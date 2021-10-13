<template>
<div class="interface-content">
    <span class="step-counter">Step 3/3</span>

    <!-- Title -->
    <h4 class="page-title mb-0">Business Category</h4>

    <!-- Verification Method -->

    <div class="business-view mb-3">
        <box-select label="Type of your business"></box-select>
        <box-select label="Business Category"></box-select>
    </div>
    <div class="mb-5">
        <p class="method-text mb-1">Do you use POS machines for your business?</p>

        <div class="method-button">
            <button class="btn">Yes</button>
            <button class="btn ml-2">No</button>
        </div>
    </div>
</div>
</template>

<script>
import BoxSelect from './BoxSelect.vue'
export default {
    components: {
        BoxSelect
    },

    data() {
        return {
            activeBtn: "Bvn",
        }
    },
}
</script>

<style lang="scss">
.business-view {
    margin-top: 1rem;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem 1rem;

    @media only screen and (max-width: 999px) {
        grid-template-columns: 1fr;
    }
}

.business-content {
    display: flex;
    flex-direction: column;

    .step-counter {
        margin: 1.5rem 0;
        color: #A5B4CB;
        font-size: 14px;
    }

}
</style>
