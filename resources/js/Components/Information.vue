<template>
    <article class="information-section">
        <section>
            <slot name="heading">
                <h1>Een heading</h1>
            </slot>
            <slot name="text">
                <p>Plaats tekst voor een omschrijving van de sectie</p>
            </slot>
        </section>
        <slot name="image">
            <img src="" alt="">
        </slot>
        <slot name="source">
            <a href="">Optioneel een link</a>
        </slot>
    </article>
</template>
<style>
p {
    width: 100%;
}

h1 {
    color: var(--secondary-color);
    font-weight: 700;
    font-size: 250%;
}

.information-section {
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 2rem;
    background: var(--primary-color);
    max-width: 50rem;
    min-width: 20vw;
    min-height: 20rem;
    border-radius: var(--element-border-radius);
}
</style>