<script>
  import Share from "./Share.svelte";
  let shareIsOpen = true;
    function toggleShare() {shareIsOpen = !shareIsOpen};
</script>

<style>
  .layout__anchor {
    position: relative;
  }
  .layout__anchor--overflow {
      position: relative;
      background-color: tomato;
    }
  .card__wrapper {
    width: 100%;
    max-width: 327px;
    border-radius: 0.625rem;
    overflow: hidden;
    box-shadow: 0px 40px 40px -10px rgba(201, 213, 225, 0.503415);
  }

  .article__image-wrapper {
    height: 200px;
    display: flex;
  }

  .article {
    height: 100%;
    display: flex;
    flex-direction: column;
  }
  button {
    border-radius: 50%;
    position: absolute;
    right:2rem;
    bottom:1rem;

    display: inline-block;
    border: none;
    margin: 0;
    padding: 0.5rem;
    background: #ECF2F8;
  }


  @media (min-width:768px) {
    .card__wrapper {
      max-width: 730px;
    }
    .article {
      flex-direction: row;
    }
    .article__image-wrapper {
      max-width: 39%;
      max-height: unset;
      height: unset;
    }
    .layout__anchor--overflow {
      display: flex;
      width: 100%;
    }
  }

  .article__content-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 100%;
  }

  em {
    display: block;
    width:100%;
  }

  /* dev utilities */
  .article__image-placeholder {
    background-color: aqua;
    height: 100%;
  }
  .article__content-placeholder {
    background-color: coral;
    height: 100%;
  }
  .article__author-placeholder{
    background-color: palevioletred;
  }
  .pink {
    background-color: pink;
  }

  .fill-white {
      fill: white;
    }
    .button-bg-dark {
      background-color: #6E8098;
    }
  
</style>
<div class="layout__anchor--overflow">
<div class="layout__anchor">
    <div class="card__wrapper pink">
      <article class="article">
      <div class="article__image-wrapper">
      <slot name="article__image" >
        <em class="article__image-placeholder">Image Placeholder</em>
      </slot>
    </div>
    <div class="article__content-wrapper">
      <slot name="article__content">
        <em class="article__content-placeholder">Content Placeholder</em>
      </slot>
      <slot name="article__author-info">
        <em class="article__author-placeholder">Author Placeholder</em>
      </slot>
    </div>
  </article>
</div>
<button on:click={toggleShare} class:button-bg-dark="{shareIsOpen}">
  <svg fill="#6E8098" xmlns="http://www.w3.org/2000/svg" width="15" height="13"><path class:fill-white="{shareIsOpen}" d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"/></svg>
</button>
</div>

</div>