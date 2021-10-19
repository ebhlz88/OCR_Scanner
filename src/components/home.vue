<template>
  <div>
      <div class="col-md-5 my-4 tt">
            <p>Upload File</p>
            <!-- <input type="file"> -->
            <button
              id="chooseimg"
              class="btn btn-primary"
              @click="bclick"
            >
              Choose Image
            </button>
            <input
              type="file"
              @change="onFileChanged"
              id="getFile"
              style="display: none"
            />
            <p>{{ filename }}</p>
            <button v-on:click="recog">recongnize</button>
            <p>{{textt}}</p>
          </div>
  </div>
</template>

<script>
import { createWorker } from 'tesseract.js';
export default {
    data(){
        return {
            textt:null
        }
    },
  methods:{
       bclick() {
      document.getElementById("getFile").click();
    },
      onFileChanged(e) {
      this.imagefile = e.target.files[0];
      this.filename = e.target.files[0].name;
    },
    recog(){
      const worker = createWorker({
});

(async () => {
  await worker.load();
  await worker.loadLanguage('eng');
  await worker.initialize('eng');
  const { data: { text } } = await worker.recognize(this.imagefile);
  await worker.terminate();
  this.textt = text
})();

    }
  }
}
</script>

<style>

</style>