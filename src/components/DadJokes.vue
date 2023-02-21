<template lang="">
  <div class="container">
    <div class="card text-end" style="width: 21rem">
      <div class="card-body">
        <h5 class="card-title">
          {{ jokes.setup }}
        </h5>
        <p class="card-text">
          {{ jokes.punchline }}
        </p>
        <button type="submit" class="btn reload" @click="reloadPage">
          Reload
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "DadJokes",
  data() {
    return {
      jokes: {},
      setup: "",
      punchLines: "",
    };
  },
  mounted() {
    fetch("https://official-joke-api.appspot.com/random_joke")
      .then((response) => response.json())
      .then((data) => (this.jokes = data));
  },
  methods: {
    reloadPage() {
      window.location.reload();
    },
  },
};
</script>
<style scoped>
.container {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.reload {
  background-color: #dc3545;
  color: white;
}

.card-title {
  font-size: 24px;
}

.card-text {
  font-weight: bold;
  font-size: 17px;
}
</style>
