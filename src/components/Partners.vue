<template>
  <div class="partners">
    <div class="container">
      <div class="columns">
        <div class="column is-3">
          <figure class="image">
            <img class="is-rounded" src="https://via.placeholder.com/150" />
          </figure>
        </div>

        <div class="column is-3">
          <figure class="image">
            <img class="is-rounded" src="https://via.placeholder.com/150" />
          </figure>
        </div>

        <div class="column is-3">
          <figure class="image">
            <img class="is-rounded" src="https://via.placeholder.com/150" />
          </figure>
        </div>

        <div class="column is-3">
          <figure class="image">
            <img class="is-rounded" src="https://via.placeholder.com/150" />
          </figure>
        </div>
      </div>

      <div class="colums is-centered">
        <div class="column">
          <router-link to="/parceiros" class="button is-info mt-6"
            >Parceiros</router-link
          >
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.partners {
  margin: 15rem auto;
}
</style>

<script>
export default {
  name: "Partners",
};
</script>
