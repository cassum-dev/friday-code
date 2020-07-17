<template>
  <carousel>
        <slide v-for="slide in promotions">
            <a :href="slide.link"><img :src="require('./../assets/' + slide.image)"></a>
        </slide>
    </carousel>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
import carrouselItems from './../data-sources/carrousel.json';

export default {
  name: 'Slider',
  components: {
    Carousel,
    Slide
  },
  data () {
    return {
        promotions: carrouselItems.promotions
    };
  }
}
</script>
