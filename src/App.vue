<template>
  <div id="app" style="background-color: dodgerblue">
    <div class="container">
      <h1>Danbury High School Class of 2007</h1>
      <div class="row">
        <ul>
          <li 
            v-for="(image, index) in images" 
            style="display: inline-block"
          >
            <img 
              v-lazy="image.src" 
              class="sizing"
              @click="openGallery(index)"
            >
          </li>
        </ul>
        <lightbox 
          :images="images" 
          ref="lightbox"
          :show-caption="true"
        ></lightbox>
      </div>
      <div class="container" style="background:#ffffff;margin-top:50px;margin-bottom:50px;">
        <div class="row">
          <div class="col-xs-12">
            <h4>Shameless Plugs</h4>
          </div>
          <div class="col-sm-4">
            <a href="https://mytennislessons.com">
              <img src="./mtl-logo.png" class="img-responsive padded">
            </a>
          </div>
          <div class="col-sm-4">
            <a href="https://fitnesstrainer.com">
              <img src="./ft-logo.png" alt="FitnessTrainer.com" class="img-responsive padded">
            </a>
          </div>
          <div class="col-sm-4">
            <a href="https://www.boardgameprices.com/">
              <img src="./bg-logo.jpg" alt="Boardgameprices" class="img-responsive padded">
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="text-center" style="padding-bottom:5px"><a href="https://twitter.com/GiveaDan">Built by Dan</a></div>
  </div>
</template>
<style scoped>
h1 {
  color: #fffaec;
  text-shadow: 0px 0px 5px orange;
  text-align: center;
}
a {
  color: white;
}
ul {
  padding-left:0;
}
.sizing {
  height: 125px;
  padding-left: 5px;
  margin-top: 5px;
}
.padded {
  padding: 10px;
  margin-top: 20px;
  max-height: 65px;
}
@media screen and (max-width: 397px) {
  .sizing {
    height: 62px;
  }
}
@media screen and (min-width: 397px) and (max-width: 600px) {
  .sizing {
    height: 100px;
  }
}
</style>

<script>

let images = [
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6055.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6055.jpg',
    caption: "<h4>What up world</h4>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6056.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6056.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6057.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6057.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6058.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6058.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6059.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6059.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6060.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6060.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6061.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6061.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6062.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6062.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6063.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6063.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6064.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6064.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6065.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6065.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6101.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6101.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6067.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6067.jpg',
    caption: "<h5>She taught me good English</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6068.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6068.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6069.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6069.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6070.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6070.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6071.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6071.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6072.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6072.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6073.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6073.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6074.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6074.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6075.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6075.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6076.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6076.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6077.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6077.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6078.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6078.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6079.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6079.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6087.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6087.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6088.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6088.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6089.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6089.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6090.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6090.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6091.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6091.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6092.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6092.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6093.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6093.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6094.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6094.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6095.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6095.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6096.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6096.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6097.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6097.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6098.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6098.jpg',
    caption: "<h5>He singing Mambo Number 5</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6099.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6099.jpg',
    caption: "<h5>She singing Mozart Symphony No. 25 in G minor</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6101.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6101.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6102.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6102.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6103.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6103.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6104.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6104.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6105.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6105.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6106.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6106.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6107.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6107.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6108.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6108.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6109.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6109.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6110.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6110.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6111.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6111.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6112.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6112.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6113.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6113.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6114.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6114.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6115.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6115.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6116.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6116.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6117.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6117.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6118.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6118.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6119.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6119.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6120.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6120.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6121.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6121.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6122.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6122.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6123.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6123.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6124.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6124.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6125.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6125.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6126.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6126.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6127.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6127.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6128.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6128.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6129.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6129.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6130.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6130.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6131.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6131.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6132.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6132.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6133.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6133.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6134.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6134.jpg',
    caption: "<h5>Name that album cover</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6135.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6135.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6136.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6136.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6137.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6137.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6138.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6138.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6139.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6139.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6140.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6140.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6141.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6141.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6142.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6142.jpg',
    caption: "<h5>Well done back to back photo!</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6143.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6143.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6144.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6144.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6145.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6145.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6146.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6146.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6147.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6147.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6148.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6148.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6149.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6149.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6150.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6150.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6151.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6151.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6152.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6152.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6153.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6153.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6154.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6154.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6155.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6155.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6156.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6156.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6157.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6157.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6158.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6158.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6159.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6159.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6160.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6160.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6161.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6161.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6162.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6162.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6163.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6163.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6164.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6164.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6165.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6165.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6166.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6166.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6167.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6167.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6168.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6168.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6169.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6169.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6170.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6170.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6171.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6171.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6172.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6172.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6173.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6173.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6174.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6174.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6175.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6175.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6176.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6176.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6177.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6177.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6178.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6178.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6179.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6179.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6180.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6180.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6181.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6181.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6182.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6182.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6183.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6183.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6184.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6184.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6185.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6185.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6186.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6186.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6191.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6191.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6192.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6192.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6193.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6193.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6194.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6194.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6195.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6195.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6196.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6196.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6197.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6197.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6198.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6198.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6199.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6199.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6200.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6200.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6201.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6201.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6202.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6202.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6203.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6203.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6204.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6204.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6205.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6205.jpg',
    caption: "<h5>Ayyy watch that hand, Mark</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6206.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6206.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6207.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6207.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6208.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6208.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6209.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6209.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6210.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6210.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6211.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6211.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6212.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6212.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6213.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6213.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6214.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6214.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6215.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6215.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6216.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6216.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6217.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6217.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6218.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6218.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6219.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6219.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6220.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6220.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6221.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6221.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6222.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6222.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6223.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6223.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6224.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6224.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6225.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6225.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6226.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6226.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6227.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6227.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6228.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6228.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6229.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6229.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6230.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6230.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6231.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6231.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6232.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6232.jpg',
    caption: "<h5>Karen forgot to be inappropriate</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6233.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6233.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6234.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6234.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6235.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6235.jpg',
    caption: "<h5>Bye Jake</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6236.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6236.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6237.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6237.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6238.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6238.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6239.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6239.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6240.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6240.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6241.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6241.jpg',
    caption: "<h5>Ryan Brown Rap Song Album Cover</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6242.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6242.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6243.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6243.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6244.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6244.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6245.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6245.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6246.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6246.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6247.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6247.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6248.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6248.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6249.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6249.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6250.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6250.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6251.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6251.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6252.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6252.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6253.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6253.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6254.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6254.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6255.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6255.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6256.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6256.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6257.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6257.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6258.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6258.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6259.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6259.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6260.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6260.jpg',
    caption: "<h5>Hand on Hips</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6261.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6261.jpg',
    caption: "<h5>Hands on Hips with a Twist</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6262.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6262.jpg',
    caption: "<h5>No one wanted to take a photo with Angelo?</h5>"
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6263.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6263.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6264.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6264.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6265.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6265.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6266.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6266.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6267.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6267.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6268.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6268.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6269.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6269.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6270.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6270.jpg'
  },
  {
    thumb: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6271.jpg',
    src: 'https://res.cloudinary.com/du5wyzaak/image/upload/v1498426478/img_6271.jpg'
  }
]

import Lightbox from 'components/Lightbox'

import siteLoading from './siteloading.gif'

export default {
  components: {
    Lightbox,
  },

  data () {
    return {
      images,
      siteLoading,
    }
  },

  methods: {
    openGallery(index) {
      this.$refs.lightbox.showImage(index)
    }
  }
}
</script>
