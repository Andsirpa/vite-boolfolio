<script>
export default {

}

</script>

<template>

    <div class="row-cols-4">
        <div class="col" v-for="project in store.projects">
            <div class="card">
                <img v-if="project.image" src="project.image" class="card-img-top" alt="...">
                <div class="card-body">
                    <h5 class="card-title">{{ project.title }}</h5>
                    <p class="card-text">{{ post.description }}</p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '/src/scss/general.scss';
</style>