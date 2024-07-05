<script>
export default {
    name: "AppHeader",
}
</script>

<template>
    <header>
        <div class="container">
            <a href="#">
                <img src="../assets/dc-logo.png" alt="Logo">
            </a>

        <nav>
            <ul>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>
                <li>
                    <a href="#">Voce Menu</a>
                </li>

            </ul>
        </nav>

        </div>
    </header>
</template>

<style lang="scss">
    header {
        padding: 20px 0;
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    ul {
        display: flex;
        gap: 20px;
        align-items: center;
    }
</style>