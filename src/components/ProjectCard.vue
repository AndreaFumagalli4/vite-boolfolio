<script>

export default {
    name: 'ProjectCard',

    props: {
        projectId: Number,
        projectTitle: String,
        projectImage: String,
        projectType: String,
        projectTechnologies: Array,

    },
}
</script>

<template>
    <article class="col-6 g-3">
        <div class="card text-center">
            <div class="card-header">
                <p>
                    Type: <span class="fw-bold">{{ projectType }}</span>
                </p>
            </div>
            <div class="card-body">
                <h3 class="mb-3">
                    {{ projectTitle }}
                </h3>
                <div class="mb-3">
                    <span v-for="technology in projectTechnologies">
                        #{{ technology.name }}
                    </span>
                </div>
                <div class="card-image mb-3">
                    <img :src="projectImage" alt="Project image" class="img-fluid">
                </div>
                <router-link :to="{name: 'single-project', params: {id: projectId } }" class="btn btn-primary">
                    More info
                </router-link>
            </div>
        </div>
    </article>
</template>

<style scoped lang="scss">
    p{
        margin: 0;
    }
</style>