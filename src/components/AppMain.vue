<script>
import axios from 'axios';
import ProjectCard from './ProjectCard.vue';

export default{
    name: 'AppMain',

    components:{
        ProjectCard,

    },

    data() {
        return {
            apiUrl: 'http://127.0.0.1:8000/api/projects',
            projectsList: [],
        }
    },

    methods: {
        getProjects(){
            axios.get(this.apiUrl, {
                params: {
                }
            })
            .then((response) => {
                this.projectsList = response.data.results.data;
                console.log(this.projectsList);
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
    <section>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1>
                        Projects
                    </h1>
                </div>
            </div>
            <div class="row">
                <div class="col-4 g-3">
                    <ProjectCard />
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">

</style>
