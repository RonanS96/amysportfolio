<script>
  import { onMount } from "svelte";
  import marked from "marked";
  import { getAboutMeMarkdown } from "../utils/aboutme.js";

  $: copied = false;
  $: copyTooltip = copied ? "Copied to clipboard!" : "Copy Email";

  const markdown = getAboutMeMarkdown();
  const text = marked(markdown);

  function copyEmail() {
    const emailAddress = document.getElementById("emailAddress");
    const tempTextArea = document.createElement("textarea");

    // create a temporary text area so the browser will allow us to copy
    tempTextArea.value = emailAddress.textContent;
    document.body.appendChild(tempTextArea);
    tempTextArea.select();
    document.execCommand("Copy");
    tempTextArea.remove();
    copied = true;
  }
</script>

<style>
  img.about-img {
    height: 600px;
    padding: 12px 24px;
  }

  .intro-text {
    font-weight: bold;
  }

  .fa {
    padding-left: 2px;
    font-size: 24px;
  }

  .fa.small-padding-right {
    padding-right: 3px;
  }

  .contact {
    text-align: center;
  }

  button.copy-button {
    cursor: pointer;
    background: none;
    border: none;
  }

  button.copy-button:focus {
    outline: none;
  }

  @media only screen and (max-width: 700px) {
    img.about-img {
      height: 300px;
    }
  }
</style>

<div class="w3-content w3-container w3-padding-64">
  <div class="section-subtitle">About Me</div>
  <div class="w3-row">
    <div class="w3-col m6 w3-center w3-padding-large">
      <img src="/images/amy2.jfif" alt="Me" class="about-img" />
    </div>
    <p class="intro-text">
      <i class="fa fa-pencil" />
      <i class="fa fa-user small-padding-right" />
    </p>
    {@html text}
  </div>
  <p class="contact">
    If you would like to contact me, please do by email:
    <button class="copy-button" on:click={copyEmail} title={copyTooltip}>
      <span class="bold" id="emailAddress">amyd996@hotmail.com</span>
      {#if copied}
        Copied!
        <i class="fa fa-check" />
      {:else}
        Copy
        <i class="fa fa-copy" />
      {/if}
    </button>
  </p>
  <p class="contact">
    <a href="/CV.pdf">See my CV here</a>
  </p>
</div>
