<template>
  <div>
    <b-alert :variant="type" dismissible show>{{ message }}</b-alert>
  </div>
</template>

<script>
export default {
  props: ['message', 'type'],
};
</script>
