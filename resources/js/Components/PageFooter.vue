<template>
    <div>
        <div v-if="canLogin" class="hidden fixed top-0 right-0 px-6 py-4 sm:block">
            <inertia-link v-if="$page.props.auth.user" href="/dashboard" class="text-sm text-gray-700 underline">
                Dashboard
            </inertia-link>

            <template v-else>
                <inertia-link :href="route('login')" class="text-sm text-gray-700 underline">
                    Log in
                </inertia-link>

                <inertia-link v-if="canRegister" :href="route('register')"
                              class="ml-4 text-sm text-gray-700 underline">
                    Register
                </inertia-link>
            </template>
        </div>
        <div class="mt-4 py-4 border-t border-blue-200 text-center">
            &copy; Al Imran Ahmed
        </div>
    </div>
</template>

<script>
export default {
    name: "PageFooter",
    props: {
        auth: Object,
        canLogin: Boolean,
        canRegister: Boolean,
    },
}
</script>

<style scoped>

</style>
