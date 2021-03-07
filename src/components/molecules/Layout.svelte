<script lang="ts">
</script>

<div class="layout-container">
  <header class="layout-header">
    <slot name="header" />
  </header>

  <div class="layout-body">
    {#if $$slots["nav-primary"] || $$slots["nav-secondary"]}
      <div class="layout-nav">
        {#if $$slots["nav-primary"]}
          <div class="layout-nav-primary">
            <slot name="nav-primary" />
          </div>
        {/if}
        {#if $$slots["nav-secondary"]}
          <div class="layout-nav-secondary">
            <slot name="nav-secondary" />
          </div>
        {/if}
      </div>
    {/if}

    <main class="layout-main">
      {#if $$slots["main-header"]}
        <header class="layout-main-header">
          <slot name="main-header" />
        </header>
      {/if}
      <div class="layout-main-content">
        <slot name="main-content" />
      </div>
      {#if $$slots["main-footer"]}
        <footer class="layout-main-footer">
          <slot name="main-footer" />
        </footer>
      {/if}
    </main>

    {#if $$slots["sub-content"]}
      <div class="layout-sub">
        {#if $$slots["sub-header"]}
          <header class="layout-sub-header">
            <slot name="sub-header" />
          </header>
        {/if}
        <div class="layout-sub-content">
          <slot name="sub-content" />
        </div>
        {#if $$slots["sub-footer"]}
          <footer class="layout-sub-footer">
            <slot name="sub-footer" />
          </footer>
        {/if}
      </div>
    {/if}
  </div>
</div>

<style lang="scss">
  @import "variables";
  $layout-header-height: 2.5rem;

  .layout-container {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
  }
  .layout-header {
    display: flex;
    flex-grow: 0;
    flex-shrink: 0;
    flex-basis: auto;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-height: 2.5rem;
    background-color: $color-bg-gray;
    border-bottom: 1px solid $color-border-gray;
    box-sizing: border-box;
  }
  .layout-body {
    display: flex;
    flex-grow: 1;
    flex-shrink: 0;
    flex-basis: auto;
    max-height: calc(100% - 2.5rem);
    height: calc(100% - 2.5rem);
  }
  .layout-nav {
    display: flex;
    background-color: $color-bg-gray;
  }
  .layout-nav-primary {
    overflow-y: auto;
    overflow-x: hidden;
    display: flex;
    width: 4rem;
    border-right: 1px solid $color-border-gray;
  }
  .layout-nav-secondary {
    overflow-y: auto;
    overflow-x: hidden;
    display: flex;
    width: 14rem;
    border-right: 1px solid $color-border-gray;
  }
  .layout-sub {
    display: flex;
    flex-direction: column;
    min-width: 250px;
    border-left: 1px solid $color-border-gray;
  }
  .layout-sub-content {
    overflow-y: auto;
    overflow-x: hidden;
    flex-grow: 1;
    flex-basis: 0;
  }
  .layout-sub-header {
    min-height: 2.5rem;
    border-bottom: 1px solid $color-border-gray;
  }
  .layout-sub-footer {
    min-height: 2.5rem;
    border-top: 1px solid $color-border-gray;
  }
  .layout-main {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
  }
  .layout-main-content {
    overflow-y: auto;
    overflow-x: hidden;
    flex-grow: 1;
    flex-basis: 0;
  }
  .layout-main-header {
    min-height: 2.5rem;
    border-bottom: 1px solid $color-border-gray;
  }
  .layout-main-footer {
    min-height: 2.5rem;
    border-top: 1px solid $color-border-gray;
  }
</style>
