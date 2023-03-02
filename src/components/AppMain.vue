<script>
import axios from 'axios';

export default{
    name: 'AppMain',

    data() {
        return {
            apiUrl: 'http://127.0.0.1:8000/api/projects',
        }
    },

    methods: {
        getProjects(){
            axios.get(this.apiUrl, {
                params: {
                }
            })
            .then(function (response) {
                console.log(response.data.results.data);
            })
            .catch(function (error) {
                console.warn(error);
            });
        }
    },

    created(){
        this.getProjects();
    }
}
</script>

<template>
    <h1>
        Projects
    </h1>
</template>

<style lang="scss">

</style>
