<template>
  <div class="row">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.panel-body {
  font-family: "Pacifico", cursive;
  font-size: 24px;
  color: #6e6e6e;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #ffe2e2;
}

.row {
  margin: 0 !important;
}
</style>
