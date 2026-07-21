<template>
    <section id="projects" class="section">
        <h2 class="section-title">Projects</h2>

        <div class="projects-container">

            <div class="project">
                <h3 class="project-title">LIMINAL</h3>
                <p class="section-text">
                    An ephemeral room-based chat application with real-time WebSocket messaging, temporary rooms, and inactivity-based expiration. Currently in development.
                </p>
                <img
                    src="/liminal.png"
                    alt="Liminal chat interface"
                    class="project-image"
                    @click="openLightbox('/liminal.png')"
                />
                <p class="project-tech">
                    <strong>Tech Stack:</strong> Vue, Spring Boot, WebSockets, Java
                </p>
                <a
                    href="https://github.com/michaelriley87/liminal-chat"
                    target="_blank"
                    class="btn"
                >
                    GitHub
                </a>
            </div>

            <div class="project">
                <h3 class="project-title">COOEE DELAY</h3>
                <p class="section-text">
                    A lightweight audio delay plugin for music production, built in C++ using JUCE, featuring tempo sync, feedback control, and tone shaping filters.
                </p>
                <img src="/cooee.png" alt="Cooee" class="project-image" @click="openLightbox('/cooee.png')" />
                <p class="project-tech">
                    <strong>Tech Stack:</strong> C++, JUCE, VST3
                </p>
                <a href="https://github.com/michaelriley87/cooee-delay-vst" target="_blank" class="btn">GitHub</a>
            </div>

            <div class="project">
                <h3 class="project-title">PLAYGRADE</h3>
                <p class="section-text">A social media platform for the critical discussion of games, film/TV, and music.</p>
                <img src="/playgrade.png" alt="PlayGrade" class="project-image" @click="openLightbox('/playgrade.png')" />
                <p class="project-tech"><strong>Tech Stack:</strong> Next.js, Mantine, Flask, PostgreSQL</p>
                <a href="https://github.com/michaelriley87/play-grade" target="_blank" class="btn">GitHub</a>
                <a href="https://play-grade.vercel.app/" target="_blank" class="btn">Live Demo</a>
            </div>

            <div class="project">
                <h3 class="project-title">KINOGUESSR</h3>
                <p class="section-text">A movie trivia game where players must guess film titles by receiving actor hints.</p>
                <img src="/kinoguessr.png" alt="Kinoguessr" class="project-image" @click="openLightbox('/kinoguessr.png')" />
                <p class="project-tech"><strong>Tech Stack:</strong> React.js</p>
                <a href="https://github.com/michaelriley87/kinoguessr" target="_blank" class="btn">GitHub</a>
                <a href="https://michaelriley87.github.io/kinoguessr/" target="_blank" class="btn">Live Demo</a>
            </div>

            <div class="project">
                <h3 class="project-title">PICKY</h3>
                <p class="section-text">An intuitive colour picker for creators who are picky about colours.</p>
                <img src="/picky.png" alt="Picky" class="project-image" @click="openLightbox('/picky.png')" />
                <p class="project-tech"><strong>Tech Stack:</strong> SvelteKit</p>
                <a href="https://github.com/michaelriley87/picky-colour-picker/" target="_blank" class="btn">GitHub</a>
                <a href="https://michaelriley87.github.io/picky-colour-picker/" target="_blank" class="btn">Live Demo</a>
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
