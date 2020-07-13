<script>
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";

  let mounted = false;

  onMount(() => {
    mounted = true;
  });
</script>

<style>
  .header-image {
    background-image: url("/images/year4/Farmhouse_External.png");
    min-height: 100%;
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.75;
  }

  .header-image .page-title {
    font-size: 50px;
    font-weight: 600;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    letter-spacing: 10px;
    color: white;
    text-transform: uppercase;
    padding: 12px 24px;
    white-space: nowrap;
    background: #f4c2c2;
    color: #000;
    border: 3px solid #000;
    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16),
      0 2px 10px 0 rgba(0, 0, 0, 0.12);
  }

  @media only screen and (max-width: 600px) {
    .header-image {
      background-attachment: scroll;
    }

    .header-image .page-title {
      font-size: 20px;
    }
  }

  @media only screen and (max-width: 310px) {
    .header-image .page-title {
      font-size: 15px;
    }
  }
</style>

<div class="header-image">
  {#if mounted}
    <div class="page-title">
      <div transition:fade={{ duration: 1500 }}>Amy Dickson</div>
    </div>
  {/if}
</div>
