<script>
  let name = "Kristen Perot";
  let bio =
    "I am a computer science student from Atlanta, Georgia. I'm really passionate about the intersection of helping people and technology, so that's what I hope to pursue out of college. I'm always looking for new adventures and experiences!";
  let hobbies = ["Baking", "Reading", "Traveling", "Coding", "Gardening"];
  import ImageCard from "./lib/ImageCard.svelte";
  let cardData = [
    {
      image: "/Flower_Market.jpg",
      title: "Flowers",
      description:
        "I love flowers because they bring beauty and color to my life.",
    },
    {
      image: "/IMG_3281.jpg",
      title: "Botanical Gardens",
      description:
        "This is me in one of my favorite places, a botanical garden. I love being surrounded by nature and the beauty of plants.",
    },
    {
      image: "/Canal.png",
      title: "Traveling",
      description:
        "I enjoy exploring new cultures and learning from the world around me.",
    },
    {
      image: "/Kayak.png",
      title: "Nature",
      description:
        "Growing up in Georgia, I have always loved being outdoors and surrounded by nature. It brings me peace and joy.",
    },
  ];
</script>

<header class="full-header" style="background-image: url('/Tulip.jpg')">
  <h1>All About Me</h1>
</header>

<div class="container">
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>{bio}</p>

  <h2>My Hobbies</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
</div>

<h2>Some of My Favorite Things</h2>
<div class="card-container">
  {#each cardData as { image, title, description }}
    <ImageCard {image} {title} {description} />
  {/each}
</div>

<style>
  .container {
    max-width: 100%;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: var(--leaf);
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
    flex-direction: row;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .card-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem;
    margin: 0;
  }
</style>
