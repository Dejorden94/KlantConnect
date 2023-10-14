<template>
    <article class="hero">
        <div>
            <h1>Meer dan afpsraken. Echte connecties.</h1>
            <p>De perfecte tool voor iedereen waarvan klanten meer zijn dan zomaar klanten.</p>
            <a href="">Bekijk alle opties</a>
        </div>
        <img src="images/information-img/Schedule-amico.svg"
            alt="Man aan het plannen met zij telefoon op een enorme calander">
    </article>
</template>
<style scoped>
h1 {
    font-weight: 700;
    font-size: 300%;
    max-width: 45rem;
}

.hero {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 80vh;
    width: 100%;
    gap: 10rem;
}

.hero>img {
    width: 50rem;
}

.hero>div>p {
    max-width: 40rem;
}

div {
    display: flex;
    gap: 1rem;
    flex-direction: column;
}

a {
    text-align: center;
    width: 70%;
    border-radius: var(--element-border-radius);
    border: 2px solid var(--secondary-color);
    padding: 1rem 2rem;
    background: var(--primary-color);
}
</style>