<template>
    <section id="home" class="home-section">
        <h1>Hi, I'm Michael Riley.</h1>
        <h2>Master's in IT, UNSW</h2>
        <p>
            I recently completed my Master's in IT at UNSW, with a strong focus on software development.
            I have experience in frontend & backend development, working with Python, JavaScript frameworks, C/C++, and
            more.
        </p>
        <p>I'm currently seeking my first software engineering role.</p>
        <a href="#projects" class="cta">View My Projects</a>
    </section>
</template>

<style>
.home-section {
    scroll-margin-top: 90px;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-size: 1.5rem;
    gap: 15px;
    padding: 0 20px;
}

h1 {
    font-size: 2.5rem;
    font-weight: bold;
}

h2 {
    font-size: 2rem;
    color: #ffdd57;
}

p {
    max-width: 600px;
    line-height: 1.6;
}

.cta {
    margin-top: 15px;
    display: inline-block;
    padding: 10px 20px;
    background-color: #ffdd57;
    color: #2b2b2b;
    font-size: 1.2rem;
    font-weight: bold;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s;
}

.cta:hover {
    background-color: #ffa500;
}
</style>
