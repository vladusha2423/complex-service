<template>
    <div id="main">
        <Navbar />
        <div class="white-space"></div>
        <Header />
        <Clients />
        <Teasers />
        <iframe src="https://yandex.ru/map-widget/v1/-/COx7YN8v" style="width: 100%; height: 500px; border: 0"></iframe>
    </div>
</template>

<script>
    import Navbar from "@/components/Navbar/Navbar";
    import Header from "@/components/Main/Header/Header";
    import Clients from "@/components/Main/Clients/Clients";
    import Teasers from "@/components/Main/Teasers/Teasers";
    export default {
        name: "Main",
        components: {Teasers, Clients, Header, Navbar}
    }
</script>

<style lang="scss" src="./Main.scss" scoped/>