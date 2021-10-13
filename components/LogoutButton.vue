<template>
<div class="logout">
    <button class="logout-button">Logout</button>
</div>
</template>

<style lang="scss">
.logout {
    display: flex;
    justify-content: flex-end;

}

.logout-button {
    background-color: #FF6774;
    border: 1px solid #FF6774;
    border-radius: 10px;
    color: #FFF;
    cursor: pointer;
    font-size: 14px;
    font-weight: bold;
    padding: 14px 23px;
    transition: all 0.2s ease-in-out;
    display: none;

    @media (min-width: 992px) {
        display: block !important;
    }
}
</style>
