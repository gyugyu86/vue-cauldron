<template>
  <div id="cauldronInput">
    <p class="inputTitle">Input Data</p>
    <textarea v-model="inputData" placeholder="Please, input data"></textarea>
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
      <button v-on:click="clickBtn">CONVERT</button>
      <button v-on:click="clickBtn">SWAP</button>
      <Modal v-if="showModal" @close="showModal = false">
        <h3 slot="header">
          Warning!
          <i class="closeModalBtn fas fa-times" @click="showModal = false"></i>
        </h3>
        <h5 slot="body">Please Input Data!</h5>
      </Modal>
    </div>
    <p class="inputTitle">Output Result</p>
    <textarea v-model="outputResult"></textarea>
  </div>
</template>

<script>
import Modal from "./common/Modal";

export default {
  data() {
    return {
      inputData: "",
      selected: "",
      outputResult: "",
      showModal: false,
    };
  },
  methods: {
    clickBtn() {
      if (this.inputData !== "") {
        // データーが入ったいる場合の機能を実装予定(copy, quoteなど)
      } else {
        // input text areaに何も入力されない状態でボタンをクリックするとアラートを出す
        this.showModal = !this.showModal;
      }
    },
  },
  components: {
    Modal,
  },
};
</script>

<style scoped>
textarea {
  height: 300px;
  width: 80%;
  font-family: Consolas, "Courier New", monospace;
}
#cauldronInput {
  color: rgb(49, 49, 153);
}
.inputTitle {
  font-size: 2rem;
  margin-bottom: 10px;
}
.selectBtn > button {
  margin-left: 5px;
}
.closeModalBtn {
  color: #42b983;
}
</style>
