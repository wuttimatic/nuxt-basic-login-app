<template>
    <div>
        <h1>Landing page</h1>
        <p></p>
        <button @click="signOut">Sign out</button>
    </div>
</template>

<script lang="ts" setup>
const { signOut } = useAuth()

</script>

<style></style>