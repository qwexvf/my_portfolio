<template>
  <div>
    <div class="uk-child-width-1-3@m uk-grid-small uk-grid-match" uk-grid>
      <div class="uk-width-1-1 uk-row-first">
        <h1 class="uk-heading-large">
          Portfolio
        </h1>
        <p class="uk-text-medium">
          My projects
        </p>
      </div>
    </div>
    <vk-grid
      gutter="medium"
      class="uk-child-width-expand@s uk-text-center uk-child-width-1-2@m"
    >
      <div>
        <div class="uk-card uk-card-default">
          <div class="uk-card-media-top">
            <img src="https://getuikit.com/docs/images/light.jpg">
          </div>
          <div class="uk-card-body">
            <h3 class="uk-card-title">
              Media Top
            </h3>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
            </p>
          </div>
        </div>
      </div>
      <div>
        <div class="uk-card uk-card-default">
          <div class="uk-card-body">
            <h3 class="uk-card-title">
              Media Bottom
            </h3>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
            </p>
          </div>
          <div class="uk-card-media-bottom">
            <img src="https://getuikit.com/docs/images/light.jpg">
          </div>
        </div>
      </div>
    </vk-grid>
  </div>
</template>

<script>
export default {}
</script>
