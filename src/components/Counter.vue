<template>
  <div>
    <div class="text_input">
      <textarea v-model="input_value"></textarea>
    </div>
    <div class="buttons">
      <div class="decide_button">
        <input v-on:click="count" type="submit" value="決定" />
      </div>
      <div class="restart_button">
        <input v-on:click="restart" type="submit" value="やり直す" />
      </div>
    </div>
    <div v-if="count_flg" class="result_text">
      実行結果: 文字数は{{ input_value.length }}でした！🌵
    </div>
    <div v-else class="result_text">実行結果: 文字数は0です！</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input_value: "",
      count_flg: false,
    }
  },
  methods: {
    count() {
      console.log(this.input_value.length)
      this.count_flg = true
    },
    restart() {
      this.input_value = ""
      this.count_flg = false
    },
  },
}
</script>

<style>
.buttons {
  display: flex;
  justify-content: center;
}
.decide_button {
  margin-top: 20px;
  margin-right: 30px;
}
.restart_button {
  margin-top: 20px;
  margin-left: 30px;
}
.text_input {
  margin-top: 30px;
  text-align: center;
}
textarea {
  width: 700px;
  height: 25em;
}
.result_text {
  margin-top: 30px;
  font-size: 30px;
  text-align: center;
}
input {
  width: 100px;
  height: 5em;
}
</style>
