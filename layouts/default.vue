<template>
    <div>
        <header>
            <nav id="desktop-nav">
                <div class="logo">
                    <h1>Prince</h1>
                </div>
        <div>
            <ul class="nav-links">
                <li><NuxtLink to="/">Home</NuxtLink></li>
                <li><NuxtLink to="/about">About</NuxtLink></li>
                <li><NuxtLink to="/projects">Projects</NuxtLink></li>
                <li><NuxtLink to="/experience">Experience</NuxtLink></li>
                <li><NuxtLink to="/contact">Contact</NuxtLink></li>
            </ul>
        </div>
            </nav>
        </header>
    </div> 
    <slot />
</template>