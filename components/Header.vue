<template>
  <header>
    <inner-column class="wide">
      <mast-head>
        <nav>
          <ul>
            <li><a href="#about-section">About</a></li>
            <li><a href="#speaker-section">Speakers</a></li>
            <li><a href="#register">Register</a></li>
            <li class="toggle">
              <ToggleLight />
            </li>
          </ul>
        </nav>
      </mast-head>
    </inner-column>
  </header>
</template>

<style scoped>
header {
  background: var(--black);
}

inner-column {
  padding: var(--space-s); /* a loose default */
}

nav ul {
  display: flex;
  gap: var(--space-l);
  justify-content: space-between;
}

nav a {
  color: var(--white);

  @media (max-width: 500px) {
    font-size: var(--step--1);
  }
}

.toggle {
  @media (max-width: 420px) {
    display: none;
  }
}
</style>
