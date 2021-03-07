<script lang="ts">
  import Layout from "./components/molecules/Layout.svelte";
  import MessageComposer from "./components/organisms/MessageComposer.svelte";
</script>

<Layout>
  <div slot="header">header</div>

  <div slot="main-header">#general</div>

  <div slot="nav-primary"></div>
  <div slot="nav-secondary"></div>

  <div slot="main-content"></div>

  <div slot="main-footer">
    <MessageComposer />
  </div>

  <div slot="sub-header">sub header</div>
  <div slot="sub-content"></div>
</Layout>

<style lang="scss">
  :global {
    html {
      height: 100%;
    }
    body {
      padding: 0;
      height: 100%;
      font-size: 16px;
      font-family: sans-serif;
    }
  }
</style>
