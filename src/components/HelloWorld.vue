<template>
  <div>
    <button @click="speech">CLICK ME</button>
  </div>
</template>

<script>
import { onMounted } from 'vue'

export default {
  setup() {
    onMounted (() => {
      console.log("sup")
    })

    function speech() {
      var u = new SpeechSynthesisUtterance();
      u.text = "こんにちは";
      u.lang = 'ja-JP';
      u.rate = 1.0;
      speechSynthesis.speak(u);

      console.log("SPEECHING")
    }

    return {
      speech
    }
  }
}
</script>
