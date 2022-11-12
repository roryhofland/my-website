<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <div class="head">
        <h3>
          <slot name="heading"></slot>
        </h3>
        <ul>
          <slot name="stack"></slot>
        </ul>
      </div>
      <p>
        <slot name="description"></slot>
      </p>
    </div>
  </div>
</template>

<style scoped>
.item {
  display: flex;
  width: 90%;
}

ul,
li {
  padding: 0;
}

ul {
  margin: -2px;
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

  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
  margin-right: 1rem;
}

.head {
  display: flex;
  align-items: center;
}

@media (min-width: 1024px) {
  .item {
    margin-top: 1rem;
  }

  i {
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 100px;
    height: 100px;
  }
}
</style>
