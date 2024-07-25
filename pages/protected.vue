<template>
    <div>
        <h1>This is protected.</h1>
        <p>status: {{ status }}</p>
    </div>
</template>

<script lang="ts" setup>
const { status } = useAuth()

</script>

<style></style>