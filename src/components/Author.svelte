
<script>
  let author = '../../images/avatar-michelle.jpg';
  export let authorName = "Anonymous";
  export let publishDate = "28 Jun 2020";
</script>

<div class="author">
  <img class="author__image" src={author} alt="">
  <div class="author__info">
    <p class="author-name">{authorName}</p>
    <time class="publish-date">{publishDate}</time>
  </div>
</div>
  
<style>
  .author{
    padding: 0 2rem 2rem;
    display: flex;
  }
  img {
    border-radius: 50%;
    width: 40px;
    height: 40%;
  }

  .author__info {
    display: flex;
    flex-direction: column;
  }

  .author-name,
  .publish-date {
    margin:0;
  }
  .publish-date {

  }
</style>