<template>
    <div v-html="svgIcon"></div>
</template>

<script>
    export default {
        props: {
            svgIcon: String,
            label: String
        }
    };
</script>