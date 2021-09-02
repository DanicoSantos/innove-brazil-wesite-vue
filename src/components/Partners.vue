<template>
  <div class="partners section">
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
          <div class="has-text-centered mt-6">
            <router-link to="/partners" class="button is-info mt-6"
              >Parceiros</router-link
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.partners {
  margin-top: 15rem;
  margin-bottom: 5rem;
}

.partners .image img {
  width: 185px;
}
</style>

<script>
export default {
  name: "Partners",
};
</script>
