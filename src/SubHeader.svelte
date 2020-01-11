<script>
  export let title;
</script>

<style>
  .header-image {
    position: relative;
    background-image: url("/images/South-View-Entire-Building.jpg");
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

  .header-image .page-title {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    letter-spacing: 10px;
    background-color: #000;
    color: white;
    text-transform: uppercase;
    padding: 12px 24px;
    white-space: nowrap;
  }
</style>

<div class="header-image">
  <div class="page-title">{title}</div>
</div>
