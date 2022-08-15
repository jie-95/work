<template>
  <div>
    <div class="divv"></div>

    <div>
      共{{ total }}条 &nbsp; 第{{ x }}页 &nbsp; 共{{ n }}页 &nbsp;
      每页显示<input v-model.number="y" type="number" @blur="totals" />条
    </div>
    <button :disabled="pgup" @click="pageUp">上一页</button>
    <button :disabled="pgdn" @click="pageDn">下一页</button>
    <div class="divv"></div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line
  data() {
    return {
      // 第x页
      x: 1,
      // 共n页
      n: "",
      // 每页显示 y 条
      y: 10,
    };
  },
  props: {
    total: {
      type: Number,
    },
  },
  methods: {
    /* eslint-disable */
    pageUp() {
      if (this.x <= 1) {
        this.pgup = true;
      }
      this.x -= 1;
    },
    pageDn() {
      if (this.n - this.x <= 0) {
        this.pgdn = true;
        this.pgup = false;
      }
      this.x += 1;
    },
    totals() {
      this.n = Math.ceil(this.total / this.y);
    },
  },
  mounted() {
    this.n = Math.floor(this.total / this.y);

    // this.y

    // this.n = this.total / 10
  },
  computed: {
    pgup() {
      if (this.x <= 1) {
        return true;
      } else {
        return false;
      }
    },
    pgdn() {
      if (this.n - this.x <= 0) {
        return true;
      } else {
        return false;
      }
    },
  },
};
</script>

<style>
.divv {
  height: 200px;
}
input {
  width: 40px;
}
</style>
