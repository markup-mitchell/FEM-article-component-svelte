<script>
  export let content_heading = "This is where the heading goes if it's properly fetched from some source or other";
  export let content_text = "This is where the text of the article teaser goes - no doubt there's some proper terminology for this, but I'm afraid I don't know what it is";
</script>

<div class="content">

  <h2>
    {content_heading}
  </h2>
  <p>
   {content_text}
  </p>
</div>

<style>
  .content {
    padding: 2rem 2rem 1.25rem;
    background-color: white;
    height: 100%;
  }
  h2 {
    margin: 0;
    font-size: 1.25rem;
    font-weight: 700;
        color: #6E8098;
        
  }
  p {
    font-size: 13px;
    color: #9DAEC2;
    margin-bottom: 0;
    line-height: 20px;
    font-weight: 500;
  }

  @media (min-width: 768px) {
    .content {
      padding: 2rem 2.5rem 0;
    }
  }
</style>