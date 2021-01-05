<template>
  <div class="home">
    <Tweet v-for="(tweet, i) in tweets" :key="i" :tweet="tweet" />
  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from "vue";
import Tweet from "../components/Tweet";
import vweets from "../vweets";
export default {
  setup() {
    const tweets = ref(vweets);
    return {
      tweets,
      Tweet,
    };
  },
};
</script>
