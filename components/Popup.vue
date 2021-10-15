<template>
<div class="popup">
    <div class="popup-content">
        <p>Your onboarding was successful</p>
        <h4>Your application is been reviewed, and you will get notified once its ready.</h4>
        <a href="https://dashboard.patronize.co/signin/">
            <button class="popup-btn" @click="$emit('close')">Login</button>
        </a>
    </div>
</div>
</template>
<script>
export default {
    emits: ['close']
}
</script>

<style lang="scss" scoped>
.popup {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background: rgba(0, 0, 0, 0.7);

    .popup-btn {
        background-color: #006AFF;
        border: 1px solid #006AFF;
        border-radius: 10px;
        color: #FFF;
        cursor: pointer;
        font-size: 14px;
        font-weight: bold;
        padding: 14px 23px;
        transition: all 0.2s ease-in-out;
        text-transform: uppercase;
        margin-top: 1rem;
    }

    .popup-content {
        background-color: #FFF;
        border-radius: 10px;
        width: 450px;
        max-width: 100%;
        padding: 1.875rem 3.125rem;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        text-align: center;

        @media only screen and (max-width: 568px) {
            width: 70vw;

        }
    }

    .popup-content h4 {
        font-size: 1.2rem;
        font-weight: 500;
        color: #141737;

    }

    .popup-content p {
        font-size: 0.8rem;
        font-weight: 500;
        color: #006AFF;
        margin: 1.25rem 0 0.625rem;
        text-transform: uppercase;
    }
}
</style>
