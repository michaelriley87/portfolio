<template>
    <section id="projects" class="section">
        <h2 class="section-title">Projects</h2>

        <div class="projects-container">
            <div class="project">
                <h3 class="project-title">PLAYGRADE</h3>
                <p class="section-text">A social media platform for the critical discussion of games, film/TV, and music.</p>
                <img src="/playgrade.png" alt="PlayGrade" class="project-image" @click="openLightbox('/playgrade.png')" />
                <p class="project-tech"><strong>Tech Stack:</strong> Next.js, Mantine, Flask, PostgreSQL</p>
                <a href="https://github.com/michaelriley87/play-grade" target="_blank" class="btn">GitHub</a>
                <p class="coming-soon">Live Demo Coming Soon</p>
            </div>

            <div class="project">
                <h3 class="project-title">KINOGUESSR</h3>
                <p class="section-text">A movie trivia game where the player must guess the movie by receiving actor hints.</p>
                <img src="/kinoguessr.png" alt="Kinoguessr" class="project-image" @click="openLightbox('/kinoguessr.png')" />
                <p class="project-tech"><strong>Tech Stack:</strong> React.js, Material UI, Django</p>
                <a href="https://github.com/michaelriley87/kinoguessr" target="_blank" class="btn">GitHub</a>
                <p class="coming-soon">Live Demo Coming Soon</p>
            </div>
        </div>

        <!-- Lightbox -->
        <div v-if="lightboxActive" class="lightbox" @click="closeLightbox">
            <img :src="lightboxImage" alt="Expanded View" class="lightbox-image" />
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            lightboxActive: false,
            lightboxImage: ''
        };
    },
    methods: {
        openLightbox(image) {
            this.lightboxImage = image;
            this.lightboxActive = true;
        },
        closeLightbox() {
            this.lightboxActive = false;
            this.lightboxImage = '';
        }
    }
};
</script>
