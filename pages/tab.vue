<template>
  <div>
    <div>
      <span :class="{ box: msg === i }" v-for="(item,i) in ['新闻','军事','娱乐']" :key="i" @click="handleClick(i)">{{item}}+{{i}}</span>
    </div>
    <div>
      <ul v-if="msg===0">
        <li>新闻</li>
        <li>新闻</li>
        <li>新闻</li>
      </ul>
      <ul v-if="msg===1">
        <li>军事</li>
        <li>军事</li>
        <li>军事</li>
      </ul>
      <ul v-if="msg===2">
        <li>娱乐</li>
        <li>娱乐</li>
        <li>娱乐</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: 0
    };
  },
  methods: {
    handleClick(index) {
      this.msg = index;
    }
  }
};
</script>

<style>
.box{ color: red}
</style>