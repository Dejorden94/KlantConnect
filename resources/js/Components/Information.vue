<template>
    <article class="information-section" :class="{ 'reverse': reverseDirection }">
        <section>
            <slot name="heading">
                <h1>Een heading</h1>
            </slot>
            <slot name="text">
                <p>Plaats tekst voor een omschrijving van de sectie</p>
            </slot>
        </section>
        <section class="illustration-section">
            <slot name="image">
                <img src="" alt="">
            </slot>
            <slot name="source">
                <a href="">Optioneel een link</a>
            </slot>
        </section>
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

.illustration-section {
    width: 100%;
}

.information-section {
    display: flex;
    align-items: center;
    gap: 2rem;
    padding: 2rem;
    background: var(--primary-color);
    max-width: 80vw;
    min-width: 20vw;
    min-height: 20rem;
    border-radius: var(--element-border-radius);
    box-shadow: 0.5rem 1rem 1rem rgba(0, 0, 0, 0.1);
}

.information-section.reverse {
    flex-direction: row-reverse;
}
</style>

<script>
export default {
    props: {
        reverseDirection: {
            type: Boolean,
            default: false
        }
    }
};
</script>
