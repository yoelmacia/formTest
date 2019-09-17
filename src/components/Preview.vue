<template>
  <div class="preview">
    <div class="name">Reusable Preview</div>
    <div class="preview-div">
      <div v-if="this.name !== `` " class="preview-name">{{this.name}}</div>
      <div v-else class="preview-name">Name</div>
      <div v-if="this.imageurl !== `` " class="preview-image-2">
        <img :src="this.imageurl" class="image" />
      </div>
      <div v-else class="preview-image">Image</div>
      <div v-if="this.description !== `` " class="preview-description">{{this.description}}</div>
      <div v-else class="preview-description">Long Name Description</div>
      <div class="preview-price-div">
        <div class="preview-price">Price</div>
        <div class="preview-total-price">
          <div class="preview-price-net">Net Price</div>
          <div class="preview-price-gross">Gross Price</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["name", "description", "imageurl", "netprice", "selected"]
};
</script>
<style>
.preview {
  display: inline-block;
  background-color: rgb(216, 216, 216);
  width: 300px;
  height: 400px;
}
.preview-div {
  text-align: center;
  margin: 0 auto;
  margin-top: 30px;
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
.image {
  width: 208px;
  height: 81px;
  border-bottom: 1px solid black;
}
.preview-image-2 {
  height: 81px;
  line-height: 30px;
  object-fit: cover;
}
</style>