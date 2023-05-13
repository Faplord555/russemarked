<template>
    <div class="flex justify-center">
        <div class="flex items-center md:flex-row space-y-8 flex-col md:justify-between px-4 py-3 w-4/5">
            <img class="h-16" src="../img/logo.png" alt="Russemarked">
            <div class="fontsize text-xl flex md:space-x-6 md:flex-row flex-col">
                <NuxtLink :to="element.route" class= "p-2 hover:text-gray-400 text-center md:p-1" v-for="element in navigationElements">{{ element.title }}</NuxtLink>
            </div>  
        </div>
    </div>
</template>

<script setup lang="ts">

interface INavigationItem {
    title: string,
    route: string
}

let props = defineProps(["title"]);

const navigationElements: INavigationItem[] = [
    {
        title: "Hjem",
        route: "/"
    },
    {
        title: "Produkter",
        route: "/produkter"
    },
    {
        title: "Gruppebestilling",
        route: "/gruppebestilling"
    },
    {
        title: "Om oss",
        route: "/om_oss"
    }
];

</script>