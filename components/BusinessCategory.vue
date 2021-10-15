<template>
<div class="interface-content">
    <span class="step-counter">Step 3/3</span>

    <!-- Title -->
    <h4 class="page-title mb-0">Business Category</h4>

    <!-- Verification Method -->

    <div class="business-view mb-3">
        <div>
            <label class="select-label mb-0">Type of your business</label>
            <div class="select-box">
                <select>
                    <option disabled selected></option>
                    <option value="1">Catering</option>
                    <option value="2">Makeup Artistry</option>
                </select>
            </div>
        </div>
        <!-- Business Category -->
        <div>
            <label class="select-label mb-0">Business Category</label>
            <div class="select-box">
                <select>
                    <option disabled selected></option>
                    <option value="1">Agriculture</option>
                    <option value="2">Beauty</option>
                </select>
            </div>
        </div>
    </div>

    <!-- POS Buttons -->
    <div class="mb-5">
        <p class="method-text mb-1">Do you use POS machines for your business?</p>

        <div class="method-button">
            <button class="btn">Yes</button>
            <button class="btn ml-2">No</button>
        </div>
    </div>
</div>
</template>

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
