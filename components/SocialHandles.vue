<template>
<div class="social-content">
    <span class="step-counter">Step 2/3</span>

    <!-- Title -->
    <h4 class="page-title mb-0">Social Handles</h4>
    <span class="step-counter">Enter your business social media handles</span>

    <!-- Verification Method -->
    <div>

        <div class="social-view mb-3">
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

.select-text {
    font-size: 12px;
    margin-bottom: 12px;
}

.method-text {
    font-size: 14px;
    margin-top: 1rem;
}

.method-button {
    display: flex;
    align-items: center;
    flex-direction: row;

    .btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        border: 1px solid #dee0e7;
        line-height: 1.2;
        border-radius: 10px;
        height: 2.5rem;
        min-width: 2.5rem;
        padding: 17px 25px;
        background: #F5F6FA;
        color: #141737;

        @media (max-width: 992px) {
            padding: 17px
        }
    }

    .btn:focus {
        background: #DCEAFF;
        border: 1px solid #006AFF;
    }
}
</style>
