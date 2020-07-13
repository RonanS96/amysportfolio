<script>
  $: navbarClass = "navbar";
  $: open = false;

  // Change style of navbar on scroll
  window.onscroll = function() {
    updateNavbarClass();
  };
  function updateNavbarClass() {
    if (
      document.body.scrollTop > 100 ||
      document.documentElement.scrollTop > 100
    ) {
      navbarClass = "navbar" + " dark";
    } else {
      navbarClass = "navbar";
    }
  }

  function toggleOpen() {
    open = !open;

    if (open) {
      navbarClass = navbarClass + " open";
    } else {
      navbarClass = navbarClass.replace("open", "");
    }
  }
</script>

<style>
  .navbar {
    z-index: 1;
    width: 100%;
    position: fixed;
    top: 0;
  }

  .navbar.dark {
    color: #000;
    background: #f4c2c2;
    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16),
      0 2px 10px 0 rgba(0, 0, 0, 0.12);
  }

  .nav-link {
    padding: 8px 16px;
    cursor: pointer;
    user-select: none;
  }

  .nav-link:hover {
    background: #bebebe;
    color: #000;
  }

  .navbar.dark .nav-link:hover {
    background: #fff;
    color: #000;
  }

  .left-links .nav-link {
    float: left;
  }

  .right-links .nav-link {
    float: right;
  }

  @media only screen and (min-width: 430px) {
    .nav-link.burger-menu {
      display: none;
    }
  }

  @media only screen and (max-width: 430px) {
    .right-links .nav-link {
      display: none;
    }

    .navbar.open .right-links .nav-link {
      display: block;
      user-select: none;
      width: 100%;
      text-align: center;
    }

    .navbar.open .right-links .nav-link.burger-menu {
      width: 50%;
      text-align: right;
    }

    .nav-link.burger-menu {
      display: block;
      width: 50%;
      text-align: right;
    }

    .navbar .nav-link.burger-menu:hover {
      background: transparent;
    }

    .navbar.dark .nav-link.burger-menu:hover {
      background: #f4c2c2;
    }
  }
</style>

<div class={navbarClass}>
  <a href="https://amy-dickson.com">
    <div class="left-links">
      <div class="nav-link">Amy Dickson</div>
    </div>
  </a>
  <div class="right-links">
    <div class="nav-link burger-menu" on:click={toggleOpen}>
      {#if open}
        <i class="fa fa-times" />
      {:else}
        <i class="fa fa-bars" />
      {/if}
    </div>
    <a href="#Projects">
      <div class="nav-link">
        <i class="fa fa-graduation-cap" />
        Projects
      </div>
    </a>
    <a href="#Portfolio">
      <div class="nav-link">
        <i class="fa fa-th" />
        Portfolio
      </div>
    </a>
  </div>
</div>
