<template>
<div class="verify-container">
    <SideImageLeft />
    <div class="verify-content">
        <LogoutButton />
        <OnboardingSteps />

        <span class="step-counter">Step 1/3</span>

        <!-- Title -->
        <h4 class="page-title mb-3">Verify Account</h4>

        <!-- Verification Method -->
        <div>
        <p class="method-text mb-1">Select a verification method</p>

        <div class="method-button">
            <button class="btn">BVN</button>
            <button class="btn ml-2">Personal Account Number</button>

        </div>

        <!-- BVN View -->
        <div class="bvn-view">
        <p class="method-text mb-0">Bank Verification Number (11-digits)</p>
        <input type="number" />
        </div>
    </div>
    </div>
</div>

</template>

<script>

</script>

<style lang="scss">
.verify-container {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 0.35fr 1fr;
  gap: 1rem 1rem;
  @media only screen and (max-width: 999px) {
        grid-template-columns: 1fr;  
  }
}



.verify-content {
    padding: 1.5rem 2rem;
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
        border: 1px solid #141737;
        line-height: 1.2;
        border-radius: 5px;
        height: 2.5rem;
        min-width: 2.5rem;
        padding: 17px 25px;   
        background: #F5F6FA;
        color: #141737;
        @media (max-width: 992px) {
            padding: 17px
        }
    }
    }

    .bvn-view {
        margin-top: 1rem;

        input {
            width: 70%;
            font-size: 1rem;
            display: inline-block;
            box-sizing: border-box;
            padding: 12px 20px;
            margin: 8px 0;           
            height: 2.5rem;
            border-radius: 0.375rem;
            border: 1px solid #838b96;
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