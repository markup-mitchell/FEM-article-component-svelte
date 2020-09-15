<script>
  import Content from './Content.svelte';
	import Author from './Author.svelte';
	import Share from './Share.svelte'

  export let data;
  const {featured_image,
		featured_image_alt,
		author_image,
		author_name,
		publish_date,
		content_heading,
		content_text } = data;
  let shareIsOpen = false;
    function toggleShare() {shareIsOpen = !shareIsOpen};
</script>

<div class="layout__anchor--overflow">
  <div class="layout__anchor">
      <div class="card__wrapper pink">
        <article class="article">
        <div class="article__image-wrapper">
        <img src={featured_image} alt={featured_image_alt}>
      </div>
      <div class="article__content-wrapper">
        <Content {content_heading} {content_text}/>
        <Author {author_name} {author_image} {publish_date}>
          <div slot="share">
            <Share {shareIsOpen} />
          </div>
          <button slot="button-slot" on:click={toggleShare} class:button-bg-dark="{shareIsOpen}">
            <svg fill="#6E8098" xmlns="http://www.w3.org/2000/svg" width="15" height="13"><path class:fill-white="{shareIsOpen}" d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"/></svg>
      
              <svg  fill="#6E8098" width="24" height="12" class="tail" class:shareIsOpen>
                <polygon points="0,0 24,0 12,12 0,0" />
              </svg>
          </button>
          </Author >
      </div>
    </article>
  </div>
  
  </div>
  </div>

<style>
  .layout__anchor--overflow {
      position: relative;
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
    display: inline-block;
    border: none;
    margin: 0;
    padding: 0.5rem;
    background: #ECF2F8;
  }
  .tail {
    display: none;
    opacity: 0;
    background-color: transparent;
  }
  

  @media (min-width:768px) {
    .layout__anchor {
    position: unset;
  }
    .layout__anchor--overflow {
      display: flex;
      width: 100%;
      max-width: 800px;
      position: relative;
    }
    .card__wrapper {
      max-width: 730px;
      height: 285px;
    }
    .article {
      flex-direction: row;
    }
    .article__image-wrapper {
      max-width: 39%;
      max-height: unset;
      height: unset;
    }

    .shareIsOpen {
      opacity: 1;
      transition: opacity 0.2s ease-in-out;
    }
  
    .tail {
      display: block;
    fill: #48556A;
    position: absolute;
    top: -28px;
    right: 5px;
    transition: opacity 0.2s ease-in-out;
    filter: drop-shadow(0px 10px 10px rgba(201, 213, 225, 0.503415));
    }
  }

  .article__content-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 100%;
  }


  .fill-white {
      fill: white;
    }
    .button-bg-dark {
      background-color: #6E8098;
    }

    img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: 0 0;
	}
  
	@media (min-width: 768px) {
		img {
			height: unset;
		}
	}
  
</style>
