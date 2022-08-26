  <template>
  <div id="foodie-journal" class="container p-3">
    <div class="row h-100">
      <div
        class="
          col-12
          title
          h-100
          text-center
          d-flex
          justify-content-center
          align-items-center
        "
      >
        <div class="line mx-3"></div>
        <h3 class="mx-3 fs-5">FOODIE JOURNAL</h3>
        <div class="line mx-3"></div>
      </div>
      <div class="col-12 d-flex justify-content-between text-center">
        <BaseCard
          v-for="journal in journals"
          :key="journal.id"
          :imageSrc="journal.img"
          :imageAlt="journal.title"
          :cardTitle="journal.title"
          :cardTime="journal.time"
        />
      </div>
    </div>
  </div>
</template>

<script>
import BaseCard from "./BaseCard.vue";
export default {
  name: "TheBanner",
  components: {
    BaseCard,
  },
  data() {
    return {
      journals: [
        {
          id: "1",
          img: require("../assets/img/journal/single-post-img3.jpg"),
          title: "Food Corner: Top Japanese Restaurant for Sushi",
          time: "By Admin | March 25, 2019",
        },
        {
          id: "2",
          img: require("../assets/img/journal/fi-roundup.jpg"),
          title: "Roundup: My New Favourite Recipes for Healty Living",
          time: "By Admin | March 25, 2019",
        },
        {
          id: "3",
          img: require("../assets/img/journal/fi-toasts.jpg"),
          title: "Why These Toasts with Tea are My New Favourite",
          time: "By Admin | March 25, 2019",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#foodie-journal {
  background-color: #fff;
  min-height: 100px;
  margin-top: -50px;
}
</style>
  
