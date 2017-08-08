<template>
  <section>
    <div class="columns">
      <div class="column is-two-thirds">
        <slot name="header">rien dans le header</slot>
      </div>
      <div id="sidebar" class="column">
        <slot name="sidebar">rien dans la sidebar</slot>
      </div>
    </div>
  </section>
</template>