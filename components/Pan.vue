<template>
<div>
    <!-- Personal Account Number -->
    <div class="pan-view mb-3">
        <base-input label="Account Number"></base-input>

        <!-- Select Bank -->
        <div>
            <label class="select-label mb-0">Select Bank</label>
            <div class="select-box">
                <select>
                    <option disabled selected></option>
                    <option value="1">United Bank for Africa</option>
                    <option value="2">Guaranty Trust Bank</option>
                    <option value="3">Access Bank</option>
                </select>
            </div>
        </div>
    </div>

</div>
</template>

<script>

</script>

<style lang="scss">
.pan-view {
    margin-top: 1rem;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem 1rem;

    @media only screen and (max-width: 999px) {
        grid-template-columns: 1fr;
    }

}
</style>
