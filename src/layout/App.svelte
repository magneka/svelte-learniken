<script>
    import Logo from "./Logo.svelte";
    import HeaderMenu from "./HeaderMenu.svelte";
    import Footer from "./Footer.svelte";
    import Content from "./Content.svelte";
</script>

<div class="wrapper">
    <div class="box logo"><Logo /></div>
    <div class="box header"><HeaderMenu /></div>
    <div class="box sidebar" />
    <div class="box content"><Content /></div>
    <div class="box footer"><Footer /></div>
</div>

<style>
    .logo {
        grid-area: logo;
    }

    .sidebar {
        grid-area: sidebar;
    }

    .content {
        grid-area: content;
    }

    .header {
        grid-area: header;
    }

    .footer {
        grid-area: footer;
    }

    .wrapper {
        display: grid;
        grid-gap: 10px;
        grid-template-columns: 300px auto;
        grid-template-rows: 90px auto 60px;
        grid-template-areas:
            "logo header"
            "sidebar content"
            "footer  footer";
        background-color: rgb(75, 0, 90);
        color: white;
        font-size: 16px;
        font-family: "Roboto", sans-serif;
        height: 100vh;
        width: 100vw;
        min-width: 1366px;
    }

    .box {
        border-radius: 0px;
        padding: 10px;
        font-size: 150%;
    }
</style>