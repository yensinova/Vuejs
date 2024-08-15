<template>
    <div class="contenedor">
        <Sidebar></Sidebar>
        <div class="contenido">
            <router-view></router-view>
        </div>
    </div>
</template>

<script setup>
    import Sidebar from '../components/Sidebar.vue';
</script>

<style>
    .contenedor{
        display: flex;
    }
    .contenido{
        flex: 1;
        padding: 20px;
    }
</style>