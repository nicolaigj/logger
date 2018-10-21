<template>
  <div class="logger-input">
    <textarea type="text" class="log-input"></textarea>
    <button class="btn btn-submit-log">Log</button>
  </div>
</template>

<script>
export default {
  name: 'LoggerInput'
}
</script>

<style scoped>
.logger-input {
  grid-area: content;
  display: grid;
  grid-template-columns: 1fr auto;
  grid-gap: 20px;
}

.log-input-area {
  grid-area: content;
  display: grid;
  grid-template-columns: 1fr auto;
  grid-gap: 20px;
}

.log-input{
  resize: none;
  width: 100%;
  grid-column: 1 / span 1;
  border: 2px solid var(--orange);
  border-radius: 10px;
  padding: 3px 3px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}

.btn-submit-log {
  height: 40px;
  align-self: center;
  background: var(--blue);
  color: white;
  font-weight: 500;
  font-size: 16px;
  padding: 0px 15px 0px 15px;
  border-radius: 10px;
  border: 2px solid var(--blue);

}
</style>
