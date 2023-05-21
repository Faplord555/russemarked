<template>
    <div class="fixed w-2/5 border-red-600 ">
        <div v-for="image in images" class="border-gray-200 border-2">
            <Image :image="image"></Image>
        </div>

    </div>
</template>

<script setup lang="ts">

    let images = [
        "~/assets/img/orangeHoodieFront.jpg",
        "~/assets/img/orangeHoodieBack.jpg"
    ]
</script>