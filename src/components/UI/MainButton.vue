<template>
    <a class="btn">
        <slot></slot>      
    </a>

</template>

<script>
export default {
    name: 'main-button'
}
</script>


<style lang="scss" scoped>
.btn{
    font-weight: 700;
    font-size: 16px;
    line-height: 14px;
    text-align: center;
    letter-spacing: 0.02em;
    text-transform: uppercase;
    border: 1px solid #7481FF;
    border-radius: 2px;
    margin-right: 10px;
    text-decoration: none;
    cursor: pointer;
    &:not(last-child) {
        margin-right: 20px;
    }
    &:hover {
        opacity: 0.9;
    }
}
.white {
    color: #7481FF;
    padding: 16px 17px;
    background: none;
}
.colored {
    color: white;
    background: #7481FF;
    padding: 16px 37px;
}
</style>