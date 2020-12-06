<template>
    <div class="header">
        <h1>{{pageheading}}</h1>
    </div>
</template>
<script>
export default {
    name: 'Header',
    props: ['pageheading']
}
</script> 
<style scoped>
.header {
    background: black;
    color: white;
    text-align: center;
    padding: 15px;

}

</style>