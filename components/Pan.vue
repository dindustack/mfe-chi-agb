<template>
    <div>
    <!-- Personal Account Number -->
        <div class="pan-view mb-3">
            <div>
            <label class="pan-text mb-0">Account Number</label>
            <input type="number" />
            </div>
            <div>
                <label class="pan-text mb-0">Select Bank</label>
            <input type="number" />
            </div>
        </div>

        
    </div>
</template>

<script>

</script>

<style lang="scss">
.pan-text {
    font-size: 14px;
    margin-top: 1rem;
}

.pan-view {
        margin-top: 1rem;
        display: grid;
         grid-template-columns: repeat(2, 1fr);
         gap: 1rem 1rem;
  @media only screen and (max-width: 999px) {
        grid-template-columns: 1fr;  
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