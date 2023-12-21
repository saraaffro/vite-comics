<script>
export default {
    name: "AppMain"
}
</script>

<template>
    <main>
        <div class="container">
            <h2>MAIN</h2>
        </div>

    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

main {
    background-color: black;
    color: white;
    // debug
    padding: 50px;
    text-align: center;
}
</style>