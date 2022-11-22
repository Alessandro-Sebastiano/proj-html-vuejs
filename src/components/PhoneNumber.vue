<template>
    <div class="phone-box">
        <a href="#">
            <span><i class="fa-solid fa-phone"></i>(555) 802-1234</span>
        </a>
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
    border-radius: 8px;
    font-weight: 600;

    span {
        font-size: 1.1rem;

        i {
            margin-right: 12px;
            color: $orange;
        }
    }
}
</style>