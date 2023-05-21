<template>
    <div class="w-4/5 m-auto">
        test
        <LiveEditor :images="images"></LiveEditor>
    </div>
</template>

<script setup lang="ts">

    const route = useRoute();

    const productId = route.params.id;

    const images: Ref<string[]> = ref([]);

    if(productId == "1") {
        images.value.push("logo.png")
        //imageUrls.value.push("~/assets/img/orangeHoodieFront.jpg");
        //imageUrls.value.push("~/assets/img/orangeHoodieBack.jpg");
    }

</script>