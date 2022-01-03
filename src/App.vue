<template>
  <div>
    <div class="title_text">
      {{ title_text }}
    </div>
    <div class="explan_text">
      文字数をカウントします。下の欄に文字数の知りたい文章を入れ、決定ボタンで実行します。
    </div>
    <Counter />
  </div>
</template>

<script>
import Counter from "@/components/Counter.vue"
export default {
  components: {
    Counter,
  },
  data() {
    return {
      title_text: "文字数カウンター⏱",
    }
  },
}
</script>

<style>
.title_text {
  margin-top: 60px;
  text-align: center;
  font-size: 3rem;
}
.explan_text {
  margin-top: 10px;
  text-align: center;
}
/* div {
  text-align: center;
} */
</style>
