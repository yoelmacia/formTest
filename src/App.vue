<template>
  <div id="app">
    <div class="dad">
      <div class="builder">
        <div class="name">Builder</div>
        <form class="form-builder">
          <label class="label-name">Name</label>
          <input class="input-name" v-model="name" type="text" placeholder="Name" />
          <label class="label-name">Description</label>
          <input class="input-name" v-model="description" type="text" placeholder="Description" />
          <label class="label-name">Image Url</label>
          <input class="input-name" v-model="imageurl" type="text" placeholder="Image Url" />
          <label class="label-name">Price Calculator</label>
          <input class="input-name" v-model="netprice" type="text" placeholder="Net Price" />
          <select class="input-name" v-model="selected">
            <option disabled value>Please select one</option>
            <option>Euros</option>
            <option>Dollar</option>
            <option>Pounds</option>
          </select>
        </form>
      </div>
      <div class="preview">
        <div class="name">Reusable Preview</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  components: {},
  data() {
    return {
      name: "",
      description: "",
      imageurl: "",
      netprice: "",
      selected: ""
    };
  }
};
</script>

<style>
.builder {
  display: inline-block;
  background-color: rgb(245, 245, 245);
  width: 300px;
  height: 400px;
}
.preview {
  display: inline-block;
  background-color: rgb(216, 216, 216);
  width: 300px;
  height: 400px;
}
.dad {
  height: 650px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.name {
  padding-top: 17px;
  padding-left: 22px;
  font-size: 20px;
  font-family: Tahoma;
}
.label-name {
  margin-top: 10px;
  padding-left: 22px;
  font-size: 15px;
  font-family: Tahoma;
}
.form-builder {
  display: flex;
  flex-direction: column;
}
.input-name {
  margin-left: 22px;
  width: 200px;
}
label {
  display: block;
}
</style>
