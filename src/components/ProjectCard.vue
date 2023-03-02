<script>
export default {
    name: 'ProjectCard',

    props: {
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
                <h3>
                    {{ projectTitle }}
                </h3>
                <div class="mt-4">
                    <span v-for="technology in projectTechnologies">
                        #{{ technology.name }}
                    </span>
                </div>
                <img :src="projectImage" alt="Project image">
            </div>
        </div>
    </article>
</template>

<style lang="scss">
    
</style>