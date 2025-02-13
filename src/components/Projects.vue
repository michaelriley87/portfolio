<template>
    <section id="projects" class="projects">
        <h2>Projects</h2>

        <div class="project">
            <h3>PlayGrade</h3>
            <p>A social media platform for the critical discussion of games, film/TV, and music.</p>
            <img src="/playgrade.png" alt="PlayGrade" class="project-image" @click="openLightbox('/playgrade.png')" />
            <p class="tech-stack"><strong>Tech Stack:</strong> Next.js, Mantine, Flask, PostgreSQL</p>
            <a href="https://github.com/michaelriley87/play-grade" target="_blank" class="cta">GitHub</a>
            <p class="coming-soon">Live Demo Coming Soon</p>
        </div>

        <div class="project">
            <h3>Kinoguessr</h3>
            <p>A movie trivia game where the player must guess the movie by receiving actor hints.</p>
            <img src="/kinoguessr.png" alt="Kinoguessr" class="project-image"
                @click="openLightbox('/kinoguessr.png')" />
            <p class="tech-stack"><strong>Tech Stack:</strong> React.js, Material UI, Django</p>
            <a href="https://github.com/michaelriley87/kinoguessr" target="_blank" class="cta">GitHub</a>
            <p class="coming-soon">Live Demo Coming Soon</p>
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

<style scoped>
.projects {
    text-align: center;
    padding: 50px 20px;
    scroll-margin-top: 90px;
}

.project {
    margin-bottom: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.project-image {
    max-width: 70%;
    max-height: 500px;
    width: auto;
    height: auto;
    display: block;
    margin: 10px 0;
    border-radius: 10px;
    border: 3px solid #333;
    padding: 5px;
    background: #fff;
    cursor: pointer;
    transition: transform 0.2s ease-in-out;
}

.project-image:hover {
    transform: scale(1.05);
}

.lightbox {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 1000;
}

.lightbox-image {
    max-width: 90%;
    max-height: 90%;
    border-radius: 10px;
    border: 5px solid #fff;
}

.lightbox:hover {
    cursor: pointer;
}

.tech-stack {
    font-size: 1rem;
    font-weight: bold;
    margin-top: 5px;
}

.cta {
    margin: 10px 5px;
    display: inline-block;
    padding: 10px 20px;
    background-color: #ffdd57;
    color: #2b2b2b;
    font-size: 1rem;
    font-weight: bold;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s;
}

.cta:hover {
    background-color: #ffa500;
}

.coming-soon {
    font-size: 1rem;
    font-weight: bold;
    color: #ffdd57;
    margin-top: 10px;
}
</style>
