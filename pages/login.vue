<template>
    <div>
        <h1>Login Page</h1>
        <h3>Status: {{ status }}</h3>
        <form @submit.prevent="userSignIn">
            <label for="username">Username:</label>
            <input type="text"
                   v-model="username"
                   id="username"
                   name="username">
            <br>
            <label for="password">Password:</label>
            <input type="password"
                   id="password"
                   v-model="password"
                   name="password">
            <br>
            <button type="submit">Login</button>
        </form>
    </div>
</template>

<script lang="ts" setup>
definePageMeta({
    auth: {
        unauthenticatedOnly: true,
        navigateAuthenticatedTo: '/protected',
    },
})

const { status, signIn } = useAuth()
const username = ref('')
const password = ref('')
const userSignIn = async () => {
    console.log('signing in');

    await signIn("credentials", { username: username.value, password: password.value })
}

</script>

<style></style>