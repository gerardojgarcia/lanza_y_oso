<script setup></script>

<template>
    <header
        class="flex w-full justify-between px-4 items-center p-2 fixed top-0 bg-white"
    >
        <img
            src="/lanzayoso_logo_small.png"
            alt="lanza y oso logo"
            width="75px"
        />
        <nav class="flex space-x-6">
            <NuxtLink to="/">Home</NuxtLink>
            <NuxtLink to="/art">Art</NuxtLink>
            <NuxtLink to="/furniture">Furniture</NuxtLink>
        </nav>
        <NuxtLink to="#contact">Contact</NuxtLink>
    </header>
</template>
