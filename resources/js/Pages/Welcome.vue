<template>
    <div>
        <div class="border-b border-blue-200 mb-3">
            <div class="mx-6 sm:mx-20 md:mx-32 lg:mx-56 px-1 sm:px-10 md:px-16 lg:px-16 xl:px-32">
                <nav-bar></nav-bar>
            </div>
        </div>

        <div class="mx-6 sm:mx-20 md:mx-32 lg:mx-56 px-1 sm:px-10 md:px-16 lg:px-16 xl:px-32">
            <list-card></list-card>
        </div>

        <page-footer></page-footer>
    </div>
</template>

<script>
import NavBar from "@/Components/NavBar";
import ListCard from "@/Components/Article/ListCard";
import PageFooter from "@/Components/PageFooter";

export default {
    components: {PageFooter, ListCard, NavBar},
    props: {
        auth: Object,
        canLogin: Boolean,
        canRegister: Boolean,
        errors: Object,
        laravelVersion: String,
        phpVersion: String,
    }
}
</script>
