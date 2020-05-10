<template>
<!-- Copied from V3 -->
  <div class="nav">
    <a href="#about" class="nav__link">About Me</a>
    <a href="#skills" class="nav__link">Skills</a>
    <a href="#projects" class="nav__link">Projects</a>
    <a href="#interests" class="nav__link">Interests</a>
    <a href="#more" class="nav__link">More Info</a>
  </div>
</template>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
/* Copied from V3 */
.nav {
    display: flex;
    width: 40%;
    position: fixed;
    z-index: 5;
    top: 0;
    right: 0;
    padding: 0.5rem 1.25rem;
    background-color: $color-grey-900;
    border-bottom-left-radius: 0.5rem;
}

.nav__link {
    color: $color-grey-100;
    margin: auto;
    text-decoration: none;
}

.nav__link:hover {
    font-weight: 500;
    color: $color-yellow-400;
}

@media (max-width: 767px) {
    /* write css code here - mobile */
    .nav {
        width: 100%;
        left: 50%;
        transform: translateX(-50%);
        border-bottom-right-radius: 0.5rem;
    }
}
</style>