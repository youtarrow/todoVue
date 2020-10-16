// nav

<template>
  <ul class="nav__list nav__list--option d-flex justify-content-around">
    <li class="listItem">
      <nuxt-link active-class="link-active" to="/" exact>TOP</nuxt-link>
    </li>
    <li class="listItem">
      <nuxt-link active-class="link-active" to="/about" exact>ABOUT</nuxt-link>
    </li>
    <li class="listItem">
      <nuxt-link active-class="link-active" to="/portfolio" exact
        >PORTFOLIO</nuxt-link
      >
    </li>
  </ul>
</template>
