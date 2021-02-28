<div class="layout-container">
  <header class="layout-header">
    <slot name="header" />
  </header>

  <div class="layout-body">
    <div class="layout-nav">
      <slot name="nav" />
    </div>

    <main class="layout-main">
      <slot name="main" />
    </main>

    <div class="layout-sub">
      <slot name="sub" />
    </div>
  </div>
</div>

<style lang="scss">
  @import "variables";

  .layout-container {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
  }
  .layout-header {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-height: 2.5rem;
    background-color: $color-bg-gray;
    border-bottom: 1px solid $color-border-gray;
  }
  .layout-body {
    display: flex;
    flex-grow: 1;
  }
  .layout-nav {
    min-width: 250px;
    background-color: $color-bg-gray;
  }
  .layout-sub {
    min-width: 250px;
    border-left: 1px solid $color-border-gray;
  }
  .layout-main {
    flex-grow: 1;
  }
</style>
