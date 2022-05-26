<template>
  <div id="uploadbox">
    <label class="uploadLabel">
      <input
        @change="handleChange"
        id="fileuploadinput"
        type="file"
        class="uploadButton"
      />
    </label>
  </div>
</template>

<script>
import Chart1 from "@/components/chart1.vue";
export default {
  name: "fileupload",
  data() {
    return {
      bardata: [],
    };
  },
  methods: {
    handleChange(event) {
      let files = event.target.files;
      let file = files[0];
      let reader = new FileReader();

      reader.onload = (e) => {
        const file = e.target.result;
        const lines = file.split(/\r\n|\n/);
        this.bardata = lines.join("\n");
      };

      reader.onerror = (e) => alert(e.target.error.name);

      reader.readAsText(file);
    },
  },
  components: {
    Chart1,
  },
};
document.onload = () => {
  let input = document.getElementById("fileuploadinput");

  // let files = input.files
};
</script>

<style>
div {
  margin: 0 auto;
  align-content: center;
  display: flex;
  flex-flow: column;
  justify-content: center;
  margin-top: 10px;
  text-align: center;
}
.uploadLabel {
  border: 1px solid #ccc;
  display: inline-block;
  padding: 7px 15px;
  cursor: pointer;
  border-radius: 5px;
}
</style>
