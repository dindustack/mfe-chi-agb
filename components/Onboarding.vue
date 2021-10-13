<template>
<div class="onboarding-container">
    <SideImageLeft />
    <div class="onboarding-content">
        <LogoutButton />
        <!-- Onboarding steps  -->
        <div class="steps-container">
            <div class="content" :class="[length >= 1 ? activeClass : disableClass]">
                <span class="content-number">1</span>
                <span class="content-text">Verify Account</span>
            </div>

            <div class="content" :class="[length >= 2 ? activeClass : disableClass]">
                <span class="content-number">2</span>
                <span class="content-text">Social Handles</span>
            </div>

            <div class="content" :class="[length >= 3 ? activeClass : disableClass]">
                <span class="content-number">3</span>
                <span class="content-text">Business Categories</span>
            </div>

        </div>
        <!-- Verify Account -->
        <div v-if="length==1">
            <VerifyAccount />
            <bottom-button button-text="Continue" @clicked="gonext"></bottom-button>
        </div>

        <!-- SocialHandles -->
        <div v-if="length==2">
            <SocialHandles />
            <bottom-button button-text="Confirm Social Handles" @clicked="gonext"></bottom-button>
        </div>

        <!-- Business Category -->
        <div v-if="length==3">
            <BusinessCategory />
            <bottom-button button-text="Complete" @clicked="gonext"></bottom-button>
        </div>
    </div>
</div>
</template>

<script>
export default {

    data() {
        return {
            length: 1,
            isActive: false,
            activeClass: 'active',
            disableClass: 'disable'
        }
    },
    methods: {
        goback() {
            if (this.length <= 3 && this.length >= 2) {
                this.length = this.length - 1
            }
        },
        gonext() {
            if (this.length <= 2 || this.length <= 1) {
                this.length = this.length + 1
            }
        }
    }
}
</script>

<style lang="scss">
.onboarding-container {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 0.35fr 1fr;
    gap: 1rem 1rem;

    @media only screen and (max-width: 999px) {
        grid-template-columns: 1fr;
    }
}

.onboarding-content {
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

.steps-container {
    display: flex;
    align-items: center;
    flex-direction: row;
    margin-top: 0.3rem;

    .content {
        display: flex;
        align-items: baseline;
        margin-right: 45px;
    }

    .content-number {
        height: 40px;
        width: 40px;
        flex-grow: 1;
        background-color: #E4E9EF;
        border-radius: 3px;
        color: #A5B4CB;
        font-weight: 700;
        font-size: 16px;
        line-height: 1;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .content-number.active {
        border-color: #006AFF;
        background-color: #006AFF;
        color: #FFF;
    }

    .content-text {
        display: none;
        margin-left: 0.5rem;
        color: #A5B4CB;
        font-weight: 500;
        font-size: 18px;

        @media (min-width: 992px) {
            display: block !important;
        }
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
}
</style>
