<script setup>
const socials = ref([
  {
    name: "Presentation",
    link: "https://drive.google.com/file/d/1t4aTGJThBM_6ez_wcC_5gmh46j0IcLtn/view?usp=sharing",
  },
  {
    name: "X",
    link: "https://x.com/DeSciWorld",
  },
  {
    name: "LinkedIn",
    link: "https://www.linkedin.com/company/desciworld",
  },
  {
    name: "Discord",
    link: "https://discord.gg/3X5YzJ9",
  },
  {
    name: "Telegram",
    link: "https://t.me/DeSciWorld",
  },
]);

const hypes = ref([
  "Incubate DeSci in Bengaluru",
  "Expert Talks and Panels",
  "Guided Workshops",
  "Ideate and Innovate",
  "Grow your Network",
  "Have Fun!",
]);
</script>

<template>
  <section id="about-section" class="about points">
    <inner-column>
      <h2 class="loud-voice">Decentralised Science showcases in Bengaluru</h2>
      <p class="attention-voice">
        Join us for 2 days of exploring the potential of DeSci tooling during
        <mark class="invert"
          ><NuxtLink class="text" to="https://indiablockchainweek.com/"
            >India Blockchain Week</NuxtLink
          ></mark
        >, Academics, students, industry professionals, open science enthusiasts
        and policymakers can all find utility with this growing technical
        movement.
      </p>
      <ul class="socials">
        <li v-for="social in socials" class="social">
          <NuxtLink class="text notice-voice" :to="social.link">{{
            social.name
          }}</NuxtLink>
        </li>
      </ul>
      <ul class="hype">
        <li v-for="hype in hypes" class="firm-voice">{{ hype }}</li>
      </ul>
    </inner-column>
  </section>
</template>

<style scoped>
section.about {
  padding: var(--space-l) 0;
}

inner-column {
  display: grid;

  gap: var(--space-2xl);
  justify-content: space-between;

  @media (min-width: 770px) {
    grid-template-columns: 1fr 0.2fr;
  }
}

h2 {
  text-align: center;
  grid-column: 1 / -1;
  font-size: var(--step-3);
}

p {
  @media (min-width: 770px) {
    grid-column: 1;
  }
}

h2 + p {
  margin-top: unset;
}
p + p {
  margin-top: unset;
}

.socials {
  display: flex;
  align-items: start;
  gap: var(--space-s);
  flex-wrap: wrap;

  @media (min-width: 770px) {
    align-self: start;
    grid-row: 2;
    grid-column: 2;
    display: grid;
  }
}

li.social {
  /* filter: invert(1); */
  justify-self: start;
}

ul.hype {
  display: grid;
  gap: var(--space-s);
  grid-column: 1 / -1;
}

.hype li {
  font-family: var(--font2);

  white-space: nowrap;
  color: var(--white);
  border-radius: 500px;

  padding: 0.5em;
  padding-left: 2em;

  background: var(--black);

  background-image: url(data:image/svg+xml;utf8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20viewBox%3D%220%200%2064%2064%22%3E%3Cpath%20d%3D%22M%2010%2036%20L%2024%2050%20L%2056%2018%22%20fill%3D%22transparent%22%20stroke-width%3D%226%22%20stroke%3D%22%23FFFFFF%22%20stroke-linecap%3D%22round%22%20stroke-linejoin%3D%22round%22%20stroke-dasharray%3D%22%22%3E%3C%2Fpath%3E%3C%2Fsvg%3E);
  background-size: 5%;
  background-position: center left 0.5em;
  background-repeat: no-repeat;

  @media (max-width: 420px) {
    font-size: var(--step-0);
  }
}
</style>
