<script>
export default {
    data() {
        return {
            title: 'Ciao ragazzi'
        };
    },
};
</script>

<template>
    <header>
        <h1 class="main-title">
            {{ title }}
        </h1>
    </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/header" as *;
</style>
