<script>
  import SubHeader from "../SubHeader.svelte";
</script>

<style>
  p.intro {
    text-align: center;
  }

  .portfolio-image img {
    max-width: 100%;
  }

  @media only screen and (min-width: 1300px) {
    .section {
      padding: 30px 220px;
    }
  }

  @media only screen and (max-width: 900px) {
    .section {
      padding-right: 0;
      padding-left: 0;
    }
  }

  @media only screen and (max-width: 600px) {
    .portfolio-image {
      padding-left: 15px;
      padding-right: 15px;
      padding-bottom: 15px;
    }
  }
</style>

<div id="Portfolio" />
<SubHeader className="header-image site-plan" title="Portfolio" />
<div class="section">
  <p class="intro">
    Find out more about me and some of the work I have done in my portfolio
    <a href="/Portfolio/Portfolio.pdf">here</a>
  </p>
  <div class="portfolio-image">
    <a href="/Portfolio/Portfolio.pdf">
      <img src="/Portfolio/PortfolioFront.JPG" alt="View my portfolio here" />
    </a>
  </div>
</div>
