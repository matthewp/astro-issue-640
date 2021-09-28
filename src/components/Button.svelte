<script>
  function toggle() {
    const html = window.document.head.parentElement
    const dark = html.classList.toggle('dark')
    const theme = dark ? 'dark' : 'light'
    localStorage.setItem('theme', theme)
  }

  if (!import.meta.env.SSR) {
    const theme = localStorage.getItem('theme')
    if (theme === 'dark') toggle()
  }
</script>

<button id="theme-switch" aria-label="Trocar tema" on:click={toggle}>
  Click me
</button>