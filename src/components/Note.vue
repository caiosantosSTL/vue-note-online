<script setup>
import fsx from "file-saver";
import { ref } from "vue";
function outFile() {
  const txt = document.querySelector("#txtarea").value;

  const blob = new Blob([txt], { type: "text/plain;charset=utf-8" });
  fsx.saveAs(blob, "out.txt");

  console.log(txt);

}

  const valueTextArea =  ref('') 

</script>

<template>
  <div class="tab">
    <div v-if="valueTextArea === ''">
      <p>Write something to save it</p>
    </div>
    <div v-else>
      <div @click="outFile()" class="btn">save text</div>
    </div>
  </div>
  <textarea
    name=""
    id="txtarea"
    cols="30"
    rows="10"
    maxlength="1500"
    placeholder="Write here"
    v-model="valueTextArea"
  ></textarea>
</template>

<style scoped>
#txtarea {
  padding: 30px;
  font-size: 26px;
  -webkit-box-shadow: 9px 8px 12px 1px rgba(0, 0, 0, 0.38);
  box-shadow: 9px 8px 12px 1px rgba(0, 0, 0, 0.38);
  resize: none;
  width: 100%;
  height: 100%;
  border-radius: 10px;
}

.tab {
  display: flex;
  justify-content: center;
  align-items: center;
  width: auto;
  margin: 10px;
  height: 80px;
}
.btn {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-content: center;
  background-color: rgb(74, 166, 43);
  height: auto;
  border-radius: 10px;
  padding: 10px;
  cursor: pointer;
  color: white;
  transition-delay: 100ms;
}
.btn:hover {
  background-color: rgb(38, 87, 22);
  transform: translateY(-5px);
}
</style>