<script setup lang="ts">
import { useAuth0 } from "@auth0/auth0-vue"

const { logout } = useAuth0();

const handleLogout = () => {
    logout({logoutParams: {returnTo: window.location.origin}})
}
</script>

<template>
    <div>
        <button @click="handleLogout">Logout</button>
    </div>
</template>