<template>
    <q-layout view="lHh Lpr lFf">
        <q-header>
            <title-bar :title="title" :back="back"/>
        </q-header>

        <q-page-container>
            <router-view />
        </q-page-container>

        <q-footer>
            <tab-navigation/>
        </q-footer>
    </q-layout>
</template>

<script>
    import TabNavigation from "../components/TabNavigation";
    import TitleBar from '../components/TitleBar'

    export default {
        name: 'MyLayout',
        components: {
            TabNavigation,
            TitleBar,
        },
        computed: {
            title() {
                return this.$route.meta.title;
            },
            back() {
                return this.$route.meta.back;
            },
        },
    }
</script>
