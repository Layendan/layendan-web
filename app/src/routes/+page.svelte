<script>
  import Fa from 'svelte-fa';
  import {
    faGithub,
    faDiscord,
    faLinkedin
  } from '@fortawesome/free-brands-svg-icons';
</script>

<svelte:head>
  <title>Layendan</title>
  <meta property="og:title" content="Layendan" />
  <meta property="og:description" content="Please hire me 🙏" />
  <meta property="og:type" content="website" />
  <meta property="og:image" content="https://layendan.dev/imgs/home.png" />
  <meta property="og:image:alt" content="layendan.dev" />
  <meta property="og:url" content="https://layendan.dev" />
  <meta name="twitter:card" content="summary_large_image" />
  <meta property="og:site_name" content="Layendan" />
  <meta name="twitter:image:alt" content="layendan.dev" />
  <meta name="twitter:creator" content="@layendan" />
</svelte:head>

<div class="grid h-screen w-screen place-items-center">
  <div class="flex flex-col gap-4 text-center">
    <h1 class="text-5xl font-bold">Layendan</h1>
    <p>please hire me 🙏</p>
    <a
      href="https://github.com/Layendan"
      target="_blank"
      rel="noopener noreferrer"
      class="btn btn-link btn-lg"
    >
      <Fa icon={faGithub} />
      Github
    </a>
    <a href="discord://-/users/235566430693752832" class="btn btn-link btn-lg">
      <Fa icon={faDiscord} />
      layendan
    </a>
    <a
      href="https://www.linkedin.com/in/aidan-labourdette/"
      target="_blank"
      rel="noopener noreferrer"
      class="btn btn-link btn-lg"
    >
      <Fa icon={faLinkedin} />
      LinkedIn
    </a>
  </div>
</div>
