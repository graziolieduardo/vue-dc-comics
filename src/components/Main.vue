<template>
    <div>
        <div class="main-top">
            <div class="wrapper">
                <h1>Content goes here</h1>
            </div>
        </div>
        <div class="main-bottom">
            <div class="wrapper">
                <ul>
                    <li></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Main'
}
</script>

<style scoped lang="scss">
@import '@/assets/style/var-colors';

    .main-top {
        margin: 0 auto;
        background-color: $black;

        .wrapper {
            width: 70%;
            margin: 0 auto;
        }

        h1 {
            display: flex;
            align-items: center;
            width: 100%;
            height: 150px;
            color: #fff;
        }
    }

    .main-bottom {
        width: 100%;
        height: 150px;
        background-color: $primary-blue;

        .wrapper {
            width: 70%;
            margin: 0 auto;
        }
    }
</style>