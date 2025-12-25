<nav class="nav">
  <a class="left" href="/">Vivien Serve</a>
  <a class="right" href="/about">About</a>
</nav>

<style>
  .nav {
    display: flex;
    justify-content: space-between;
    align-items: baseline; 
    z-index: 10;
    padding-bottom: 4px;
    padding-top: 16px;
    border-bottom: 1px solid var(--color-highlight);
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(255, 255, 255, 0.8);
  }

  a {
    font-family: var(--font-mono);
    font-size: 18px;                    /* mobile */
    text-transform: uppercase;
    color: var(--color-highlight);
    letter-spacing: 0.5px;
    text-decoration: none;
  }

  a:hover {
    color: var(--color-primary);
  }

  /* Desktop */
  @media (min-width: 900px) {
    .nav {    
        padding-bottom: 6px;    
        padding-top: 24px;  
    }

    a {
      font-size: 20px;                 
    }
  }
</style>
