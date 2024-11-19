<script>
  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import CRMForm from './components/CRMForm.svelte'
</script>

<div class="app-container">
  <Header />
  <main>
    <CRMForm />
  </main>
  <Footer />
</div>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    min-height: 100vh;
  }

  .app-container {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  main {
    flex: 1;
    background-color: #0B6BDB;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: flex-start;
  }
</style>
