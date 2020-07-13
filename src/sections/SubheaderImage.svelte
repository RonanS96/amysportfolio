<script>
  export let title;
</script>

<style>
  .header-image {
    position: relative;
    text-align: center;
    background-image: url("/images/AT3/SouthElevation.jpg");
    min-height: 300px;
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.75;
  }

  @media only screen and (max-width: 600px) {
    .header-image {
      background-attachment: scroll;
    }
  }

  .header-image.napier {
    background-image: url("/images/napier.jpg");
  }

  .header-image .section-title {
    display: inline-block;
    letter-spacing: 10px;
    background: #f4c2c2;
    color: #000;
    border: 3px solid #000;
    text-transform: uppercase;
    padding: 12px 24px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
</style>

<div class="header-image napier">
  <div class="section-title">{title}</div>
</div>
