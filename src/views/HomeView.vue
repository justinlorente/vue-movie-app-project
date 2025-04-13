<template>
  <div class="home">
    <div class="feature-card">
      <router-link to="/movie/tt0409591">
        <img
          src="https://i5.walmartimages.com/asr/c1201863-cd23-4ad8-b94f-984a9a56e6f2_1.9231ad3387dc1b7a01084917eb70584e.jpeg"
          alt="Interstellar Poster" class="featured-img" />
        <div class="details">
          <h3>Interstellar</h3>
          <p>When Earth becomes uninhabitable in the future, a farmer and ex-NASA pilot, Joseph Cooper,
            is tasked to pilot a spacecraft, along with a team of researchers, to find a new planet for humans.</p>
        </div>
      </router-link>
    </div>
  </div>
  <form @submit.prevent="" class="search-box">
    <input type="text" placeholder="What are you looking for?" />
    <input type="submit" value="Search" />
  </form>
</template>

<script>

export default {
}
</script>

<style lang="scss">
.home {
  .feature-card {
    position: relative;

    .featured-img {
      display: block;
      width: 100%;
      height: 300px;
      object-fit: cover;

      position: relative;
      z-index: 0;
    }

    .details {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: rgba(0, 0, 0, 0.6);
      padding: 16px;
      z-index: 1;

      h3 {
        color: #FFF;
        margin-bottom: 16px;
      }

      p {
        color: #FFF;
      }
    }
  }

  .search-box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 16px;

    input {
      display: block;
      appearance: none;
      border: none;
      outline: none;
      background: none;

      &[type="text"] {
        width: 100%;
        color: #FFF;
        background-color: #496583;
        font-size: 20px;
        padding: 10px 16px;
        border-radius: 8px;
        margin-bottom: 15px;
        transition: 0.4s;

        &::placeholder {
          color: #f3f3f3;
        }

        &:focus {
          box-shadow: 0px 3px 6px rbga(0, 0, 0, 0.2);
        }

      }
    }
  }
}
</style>
