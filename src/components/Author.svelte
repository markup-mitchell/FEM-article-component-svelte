
<script>
  export let authorName = "Anonymous";
  export let publishDate = "28 Jun 2020";
  let author = '../../images/avatar-michelle.jpg';
  let shareIsOpen = true;
</script>

<div class="author-wrapper">
  <div class="author">
    <img class="author__image" src={author} alt="">
    <div class="author__info">
      <p class="author-name">{authorName}</p>
      <time class="publish-date">{publishDate}</time>
    </div>
  </div>
  <slot name="share" />  
</div>


  <style>

  .author-wrapper {
    position: relative;
  }
  .author{
    padding: 1rem 2rem;
    display: flex;
    background-color: white;
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
  }
  .publish-date {
    font-size: 12px;
  }

  

 
  @media (min-width: 768px) {
    .author {
      padding: 0 2.5rem 2rem;
      position: unset;
    }
    .author-wrapper {
      position: unset;
    }
  }
   

    
</style>