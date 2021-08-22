<script>
export default {
    name: 'NavLinks',
    props: ['url', 'text']
}
</script>

<template>
    <a :href="url">{{ text }}</a>
</template>