<template>
    <li :class="{even : index % 2 !== 0, odd: index % 2 === 0}">
        <a href="">{{ item.title }} + {{index}}</a>
        <div>{{ item.body }}</div>
    </li>
</template>

<script>

export default {
    props: {
        item: {
            type: Object,
            required: true
        },
        index : Number
    },
}
</script>

<style scoped>

</style>
