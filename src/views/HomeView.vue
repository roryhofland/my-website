<script setup lang="ts"></script>

<template>
  <main>
    <div class="item">
      <i class="fa fa-user"></i>
      <div class="details">
        <h3>About Me</h3>
        Hey! My name is <strong>Rory Hofland</strong>, I am an undergraduate
        student at the <strong>University of Toronto</strong>, and I am working
        my way towards a double major in Mathematics and Computer Science. My
        expected graduation data is <strong>April 2024</strong>.
      </div>
    </div>

    <div class="item">
      <i class="fa fa-code"></i>
      <div class="details">
        <h3>Software Development</h3>
        I began coding in <strong>Java</strong> and <strong>C++</strong> during
        high school. This introduction to computer programming greatly motivated
        me to further my knowledge and experience, so mathematical
        problem-solving became a core aspect of my working habits, which led me
        to pursue an education in STEM. Since then, I have added
        <strong>Python</strong>, <strong>HTML</strong>, <strong>CSS</strong>,
        <strong>TypeScript</strong>, <strong>C#</strong>, and
        <strong>SQL</strong> to my toolbelt, and I am constantly learning and
        looking for more skills.
      </div>
    </div>

    <div class="item">
      <i class="fa fa-star"></i>
      <div class="details">
        <h3>Other Stuff</h3>
        Other than my academic studies, I have a few hobbies that occupy the
        rest of my time. I love to read, and will devour anything science
        fiction or high fantasy. I am currently reading
        <a
          href="https://www.goodreads.com/book/show/77507.Red_Mars"
          target="_blank"
          >Red Mars</a
        >
        by Kim Stanley Robinson. I also watch movies, play video games, and
        enjoy dominating my family and friends at Settlers of Catan!
      </div>
    </div>
  </main>
</template>

<style scoped>
.item {
  margin-top: 2rem;
  margin-bottom: 2rem;
  display: flex;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;
  margin-top: 10px;
  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

@media (min-width: 1024px) {
  main {
    padding: 0 2rem 0 2rem;
  }

  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem 3rem;
  }

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
    margin-top: 0;
  }

  .item:before {
    content: " ";
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: " ";
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
