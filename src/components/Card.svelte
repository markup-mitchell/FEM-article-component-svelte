<style>
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

  
</style>

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