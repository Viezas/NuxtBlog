<template>
    <div>
        <div class="mt-10 mb-5">
            <h1 class="text-bold text-3xl text-center text-blue-600">About</h1>
        </div>
        <div class="flex items-center justify-center flex-wrap">
            <p class="text-center mb-10 text-xl">Je sais pas quoi mettre ici, alors je vais mettre une vidéo !</p>
            <div class="px-96">
                <iframe width="690" height="400" src="https://www.youtube.com/embed/k7YVxLLIuGM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>            
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : 'About',
    head: {
        title: `NuxtBlog | Home`
    }
}
</script>