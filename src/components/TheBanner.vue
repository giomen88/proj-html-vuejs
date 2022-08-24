  <template>
  <div class="container">
    <banner id="foodie-journal">
      <div class="title">
        <div></div>
        <h2>FOODIE JOURNAL</h2>
        <div></div>
      </div>
      <div class="row">
        <div class="col-4"><SmallBaseCard /></div>
        <div class="col-4"><SmallBaseCard /></div>
        <div class="col-4"><SmallBaseCard /></div>
      </div>
    </banner>
  </div>
</template>

<script>
export default {
  name: "TheBanner",
};
</script>

<style lang="scss" scoped>
#foodie-journal {
  background-color: #fff;
  position: absolute;
  top: -10%;
  right: 50%;
}
</style>
  
