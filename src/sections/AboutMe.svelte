<script>
  import { onMount } from "svelte";
  import marked from "marked";
  import { getAboutMeMarkdown } from "../utils/aboutme.js";

  $: copied = false;
  $: copyTooltip = copied ? "Copied to clipboard!" : "Copy";

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

  @media only screen and (max-width: 600px) {
    img.about-img {
      height: 300px;
    }
  }

  .intro-text {
    font-weight: bold;
  }

  .fa {
    font-size: 24px;
  }

  .fa.small-padding-right {
    padding-right: 3px;
  }

  .contact {
    text-align: center;
  }

  .copy-button {
    cursor: pointer;
  }
  .copy-button:hover {
    color: #e91e63;
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
      Amy Dickson -
      <i>Architectural Technology Student at Edinburgh Napier University</i>
    </p>
    {@html text}
  </div>
  <p class="contact">
    If you would like to contact me, please do so through my academic email
    address
    <span class="bold" id="emailAddress">40276994@live.napier.com</span>
    <i
      on:click={copyEmail}
      class="fa fa-copy copy-button"
      title={copyTooltip} />
  </p>
  <p class="contact">
    <a href="/CV.pdf">See my CV here</a>
  </p>
</div>
