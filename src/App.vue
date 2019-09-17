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
        <div class="preview-div">
          <div class="preview-name">Name</div>
          <div class="preview-image">Image</div>
          <div class="preview-description">Long Name Description</div>
          <div class="preview-price-div">
            <div class="preview-price">Price</div>
            <div class="preview-total-price">
              <div class="preview-price-net">Net Price</div>
              <div class="preview-price-gross">Gross Price</div>
            </div>
          </div>
        </div>
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
.preview-div {
  text-align: center;
  margin: 0 auto;
  margin-top: 30px;
  background-color: #8ebf42;
  width: 210px;
  height: 250px;
  border: 1px solid black;
}
.preview-name,
.preview-div,
.preview-image,
.preview-description {
  border-bottom: 1px solid black;
}
.preview-image,
.preview-description {
  height: 30px;
  line-height: 30px;
  padding: 25px;
}
.preview-image,
.preview-name {
  background-color: rgb(216, 216, 216);
}
.preview-description,
.preview-price-div {
  background-color: rgb(130, 130, 130);
  color: rgb(192, 192, 192);
}
.preview-price-div {
  width: 210px;
  height: 69px;
}
.preview-price {
  height: 69px;
  width: 105px;
  border-right: 1px solid black;
  line-height: 69px;
  float: left;
  background-color: rgb(147, 147, 147);
}
.preview-total-price {
  height: 69px;
  width: 104px;
  float: right;
  line-height: 35px;
}
</style>
