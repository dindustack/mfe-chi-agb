<template>
<div class="interface-content">
    <span class="step-counter">Step 1/3</span>

    <!-- Title -->
    <h4 class="page-title mb-0">Verify Account</h4>

    <!-- Verification Method -->
    <div>
        <p class="method-text mb-1">Select a verification method</p>

        <div class="method-button">
            <button class="btn" @click="activeBtn = 'Bvn'">BVN</button>
            <button class="btn ml-2" @click="activeBtn = 'Pan'">Personal Account Number</button>
        </div>

        <component :is="activeBtn" />

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

<style lang="scss" scoped>
.select-text {
    font-size: 12px;
    margin-bottom: 12px;
}


</style>
