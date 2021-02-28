<script lang="ts">
  import Layout from "./components/molecules/Layout.svelte";
</script>

<Layout>
  <div slot="header">header</div>
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
