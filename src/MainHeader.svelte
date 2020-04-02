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
    background-image: url("/images/AT3/SouthElevation.jpg");
    min-height: 100%;
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
  {#if mounted}
    <div class="page-title">
      <div transition:fade={{ duration: 1500 }}>Amy Dickson</div>
    </div>
  {/if}
</div>
