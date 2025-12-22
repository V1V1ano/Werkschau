<nav class="nav">
  <a class="left" href="/">&larr; Works</a>
  <a class="right" href="/about">About</a>
</nav>

<style>
  .nav {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    padding: 10px 12px;                 /* mobile */
    position: relative;
    z-index: 10;
    border-bottom: 1px solid var(--color-highlight);
  }

  a {
    font-family: var(--font-mono);
    font-size: 18px;                    /* mobile */
    text-transform: uppercase;
    color: var(--color-primary);
    letter-spacing: 0.5px;
    text-decoration: none;
  }

  a:hover {
    color: var(--color-primary);
  }

  /* Desktop */
  @media (min-width: 900px) {
    .nav {
      padding: 16px 24px;             
    }

    a {
      font-size: 20px;                 
    }
  }
</style>
