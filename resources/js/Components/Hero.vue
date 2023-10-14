<template>
    <article class="hero">
        <div>
            <h1>Meer dan afpsraken. Echte connecties.</h1>
            <a href="">Bekijk alle opties</a>
        </div>
        <img src="images/information-img/Schedule-amico.svg"
            alt="Man aan het plannen met zij telefoon op een enorme calander">
    </article>
</template>
<style scoped>
h1 {
    max-width: 25rem;
}

.hero {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 80vh;
    width: 100%;
}

.hero>img {
    width: 50rem;
}

div {
    display: flex;
    gap: 1rem;
    flex-direction: column;
}

a {
    text-align: center;
    width: 70%;
    border-radius: 1rem;
    padding: 1rem 2rem;
    background: var(--primary-color);
}
</style>