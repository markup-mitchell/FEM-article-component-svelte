
<script>
  export let author_name = "Anonymous";
  export let author_image;
  export let publish_date; 
</script>

  <div class="author-wrapper">
    <div class="author">
      <img class="author__image" src={author_image} alt={author_name}>
      <div class="author__info">
        <p class="author-name">{author_name}</p>
        <p class="publish-date">{publish_date}</p>
      </div>
      <div class="button-slot__wrapper">
        <slot name="button-slot"/>  
      </div>
    </div>
    <slot name="share"/>
  </div>



  <style>

  .author-wrapper {
    position: relative;
  }
  .author{
    padding: 1rem 2rem;
    display: flex;
    background-color: white;
    position: relative;
    align-items: center;
    font-weight: 500;
  }
  img {
    border-radius: 50%;
    width: 40px;
    height: 40%;
  }

  .author__info {
    display: flex;
    flex-direction: column;
    margin-left: 1rem;
  }

  .author-name,
  .publish-date {
    margin:0;
    color: #48556A;
    font-size: 12px;
    line-height: 1.5;
  }
  .publish-date {
    color: #9DAEC2
  }

  .button-slot__wrapper {
    position: absolute;
    right:2.5rem;
    bottom:1.2rem;
    z-index: 10;
  }
  @media (min-width: 768px) {
    .author {
      padding: 0 2.5rem 2rem;
    }
    .author-wrapper {
      position: unset;
    }
    .button-slot__wrapper {
      bottom:2.25rem;
    }
  }
</style>