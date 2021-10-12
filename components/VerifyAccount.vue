<template>
<div class="verify-container">
    <SideImageLeft />
    <div class="verify-content">
        <LogoutButton />
        <OnboardingSteps />

        <span class="step-counter">Step 1/3</span>

        <!-- Title -->
        <h4 class="page-title mb-0">Verify Account</h4>

        <!-- Verification Method -->
        <div>
        <p class="method-text mb-1">Select a verification method</p>

        <div class="method-button">
            <button class="btn">BVN</button>
            <button class="btn ml-2">Personal Account Number</button>

        </div>

        <!-- BVN View -->
        <div class="bvn-view mb-3">
        <p class="method-text mb-0">Bank Verification Number (11-digits)</p>
        <input type="number" />
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
        <bottom-button button-text="Continue"></bottom-button> 
    </div>
</div>

</template>

<script>
import BottomButton from './BottomButton.vue';
export default {
  components: { BottomButton },
    methods: {
        accordionClick () {
        const toggle = document.querySelector(".faq-toggle");

         toggle.parentNode.classList.toggle("active");
        }
    }
}

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

    @media only screen and (max-width: 999px) {
       padding: 3.5rem 2rem 
    }

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