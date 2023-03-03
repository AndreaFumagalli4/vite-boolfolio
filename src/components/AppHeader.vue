<script>

export default{
    name: 'AppHeader',

}
</script>

<template>
    <nav class="navbar navbar-expand-md">
        <div class="container">
            <a class="navbar-brand" href="#">
                Projects
            </a>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <router-link :to="{ name: 'home' }" class="nav-link active" aria-current="page">
                            Home
                        </router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{ name: 'projects' }" class="nav-link">
                            Projects
                        </router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{ name: 'about-us' }" class="nav-link">
                            About-us
                        </router-link>
                    </li>
                </ul>
                <form class="d-flex" role="search">
                    <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-info" type="submit">Search</button>
                </form>
            </div>
        </div>
    </nav>
</template>

<style scoped lang="scss">

</style>