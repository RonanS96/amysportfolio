<script>
  export let title;
  export let className;
</script>

<style>
  .header-image {
    position: relative;
    min-height: 300px;
    background-attachment: fixed;
    background-image: url("/images/year4/Flats_Internal.PNG");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.75;
  }

  .header-image.site-plan {
    background-image: url("/images/year4/(AT4)_3D_Site_Plan.png");
  }

  .header-image .page-title {
    font-size: 20px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    letter-spacing: 10px;
    background: #f4c2c2;
    color: #000;
    border: 3px solid #000;
    font-weight: 600;
    text-transform: uppercase;
    padding: 12px 24px;
    white-space: nowrap;
    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16),
      0 2px 10px 0 rgba(0, 0, 0, 0.12);
  }

  @media only screen and (max-width: 600px) {
    .header-image {
      background-attachment: scroll;
    }

    .header-image .page-title {
      font-size: 15px;
    }
  }
</style>

<div class={className}>
  <div class="page-title">{title}</div>
</div>
