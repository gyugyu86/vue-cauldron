<template>
  <div id="cauldronInput">
    <p class="inputTitle">Input Data</p>
    <textarea
      v-model="inputData"
      v-on:keyup.enter="outputBtn"
      placeholder="Please, input logs"
    ></textarea>
    <div class="selectBtn">
      <span>
        <select v-model="selected">
          <option disabled value="">Please select one</option>
          <option>copy</option>
          <option>quote</option>
          <option>line_count</option>
          <option>encode_utf8</option>
          <option>shorttrace</option>
        </select>
      </span>
      <button v-on:click="convertBtn">CONVERT</button>
      <button>SWAP</button>
    </div>
    <p class="inputTitle">Output Result</p>
    <textarea v-model="outputResult"></textarea>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      inputData: "",
      selected: "",
      outputResult: "",
    };
  },
  methods: {
    outputBtn: function() {
      console.log(this.inputData);
    },
    convertBtn: function() {
      alert("clickされました");
    },
  },
};
</script>

<style scoped>
#cauldronInput {
  color: rgb(49, 49, 153);
}

textarea {
  height: 300px;
  width: 80%;
  font-family: Consolas, "Courier New", monospace;
}
.inputTitle {
  font-size: 2rem;
  margin-bottom: 10px;
}
.selectBtn > button {
  margin-left: 5px;
}
</style>
