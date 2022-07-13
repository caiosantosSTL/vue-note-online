<script setup>
import fsx from "file-saver";
function outFile() {
  const txt = document.querySelector("#txtarea").value;

  const blob = new Blob([txt], { type: "text/plain;charset=utf-8" });
  fsx.saveAs(blob, "out.txt");

  console.log(txt);
}
</script>

<template>
  <div class="tab">
    <div @click="outFile()" class="btn">save text</div>
  </div>
  <textarea name="" id="txtarea" cols="30" rows="10" maxlength="1500" placeholder="Write here"></textarea>
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
  width: auto;
  margin: 10px;
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
}
</style>