<template>
<div class="business-content">
    <span class="step-counter">Step 3/3</span>

    <!-- Title -->
    <h4 class="page-title mb-0">Business Category</h4>

    <!-- Verification Method -->
    <div>

        <div class="business-view mb-3">
            <social-input label="Choose your Abeg Tag (required)"></social-input>
            <social-input label="Instagram"></social-input>
            <social-input label="Twitter"></social-input>

        </div>
    </div>
</div>
</template>

<script>
export default {

    data() {
        return {
            activeBtn: "Bvn",
        }
    },
}
</script>

<style lang="scss">
.social-view {
    margin-top: 1rem;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem 1rem;

    @media only screen and (max-width: 999px) {
        grid-template-columns: 1fr;
    }
}

.social-content {
    display: flex;
    flex-direction: column;

    .step-counter {
        margin: 1.5rem 0;
        color: #A5B4CB;
        font-size: 14px;
    }

}


</style>
