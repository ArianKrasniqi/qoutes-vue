<template>
  <div class="row">
    <div class="panel panel-default">
      <div class="panel-body qoute">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script></script>

<style>
.panel-body {
  font-family: "Arizonia", cursive;
  font-size: 24px;
  color: #6e6e6e;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #ffe2e2;
}
</style>
