<template>
<div>
    <!-- BVN View -->
    <div class="bvn-view mb-3">
        <base-input label="Bank Verification Number (11-digits)"></base-input>
    </div>

    <!-- Accordion -->
    <div class="accordion-container" @click="accordionClick()">
        <div class="faq">
            <h4 class="faq-title">Why we need your BVN</h4>
            <p class="faq-text">
                The Bank Verification Number (BVN) was introduced by the Central Bank of Nigeria (CBN) as a way to protect customers from identity theft, banking fraud and protect the integrity of the banking system.
            </p>

            <button class="faq-toggle">
                <i class="fas fa-chevron-down"></i>
                <i class="fas fa-times"></i>
            </button>
        </div>
    </div>
</div>
</template>

<script>
export default {
    methods: {
        accordionClick() {
            const toggle = document.querySelector(".faq-toggle");

            toggle.parentNode.classList.toggle("active");
        }
    }
}
</script>

<style lang="scss">
.method-text {
    font-size: 14px;
    margin-top: 1rem;
}

.bvn-view {
    margin-top: 1rem;

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

    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }

    input[type="number"] {
        -moz-appearance: textfield;
    }
}
</style>
