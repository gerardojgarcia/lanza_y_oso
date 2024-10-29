<script setup></script>
<template>
    <div class="grid md:grid-cols-2 mt-32 pb-12">
        <div>
            <img
                src="/profile_pic_2.png"
                alt="Img of Gerardo Garcia"
                height="900px"
                width="600px"
                class="hidden md:block"
            />
            <NuxtImg src="/lanzayoso.png" class="md:hidden" />
        </div>
        <div class="text-black space-y-4">
            <h1 class="text-5xl text-black hidden md:block">Lanza y Oso</h1>
            <p class="px-2 md:px-0 md:w-3/4">
                is a multidisciplinary art studio founded by Gerardo García.
            </p>
            <NuxtLink to="/art" class="group">
                <NuxtImg
                    src="/art/cargando_agua.webp"
                    alt="man carrying water"
                    sizes=" sm:85vw md:35vw"
                    class="hover:shadow-lg p-4 duration-300"
                />
                <p
                    class="group-hover:opacity-100 md:opacity-0 text-xl transition-opacity duration-300"
                >
                    go to art
                </p>
            </NuxtLink>
        </div>
    </div>
</template>
