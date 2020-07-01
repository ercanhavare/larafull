<template>
    <div>
        <h1 ref="myref">Hook tutorial</h1>
        <p>My name is: {{name}}</p>
    </div>
</template>

<script>
    export default {
        name: "hooks",
        data() {
            return {
                name:'ercan',
            }
        },
        beforeCreate() {
            console.log(this.name)
        },
        created() {
            // call mostly initial data from it...
            //console.log(this.$refs.myref)
            console.log('data and other function is available but not html',this.name);
        },
        mounted() {
            console.log(this.$refs.myref)
        }
    }
</script>

<style scoped>

</style>
