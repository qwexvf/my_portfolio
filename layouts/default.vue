<template>
  <div id="app">
    <nav class="uk-navbar-container uk-margin-large-bottom" uk-navbar>
      <div class="uk-navbar-left">
        <ul class="uk-navbar-nav">
          <li class="uk-active">
            <n-link to="/">
              Home
            </n-link>
          </li>
          <li class="uk-parent">
            <n-link to="/portfolio">
              Portfolio
            </n-link>
          </li>
          <li>
            <n-link to="/blog">
              Blog
            </n-link>
          </li>
        </ul>
      </div>
    </nav>
    <div class="uk-container">
      <nuxt />
    </div>
  </div>
</template>
