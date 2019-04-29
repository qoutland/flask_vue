<template>
  <div>
    <div class="container">
      <button type="button" class="btn btn-primary">{{ mssg }}</button>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Ping',
  data() {
    return {
      mssg: '',
    };
  },
  methods: {
    getMessage() {
      const path = 'http://localhost:5000/ping';
      axios.get(path)
        .then((res) => {
          this.mssg = res.data;
        })
        .catch((error) => {
          // eslint-disable-next-line
              console.error(error);
        });
    },
  },
  created() {
    this.getMessage();
  },
};
</script>
