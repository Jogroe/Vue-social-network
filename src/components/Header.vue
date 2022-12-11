<template>
    <header id="header">
        <div id="header-left">
            <h1>Twitor</h1>
        </div>
        <div>
            <h2>Dernière news</h2>
        </div>
    </header>
</template>

<script setup>

</script>

<style scoped>

#header {
    width: 100%;
    height: 10vh;
    background-color: #15202B;
    display: flex;
    flex-direction: row;
}

#header-left {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-left: 30px;
}

#header-right {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    padding-right: 10px;
}

#img-vue {
    width: 50px;
    height: 50px;
    margin-left: 10px;
}

</style>