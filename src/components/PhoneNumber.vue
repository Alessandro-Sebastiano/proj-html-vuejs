<template>
    <div class="phone-box">
        <span><i class="fa-solid fa-phone"></i></span>
        <span>(555) 802-1234</span>
    </div>
</template>

<script>
export default {
    name: 'PhoneNumber',
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.phone-box {
    padding: 6px 18px;
    display: flex;
    align-items: center;
    border-radius: 8px;
    font-weight: 600;

    span {
        display: block;

        i {
            margin-right: 12px;
            color: $orange;
        }
    }
}
</style>