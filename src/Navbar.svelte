<script>
  $: navbarClass = "navbar";

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
</script>

<style>
  .navbar {
    z-index: 1;
    width: 100%;
    position: fixed;
    top: 0;
  }

  .navbar.dark {
    color: #fff;
    background: #616161;
    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16),
      0 2px 10px 0 rgba(0, 0, 0, 0.12);
  }

  .navbar.dark a {
    color: white;
  }

  .nav-link {
    padding: 8px 16px;
    cursor: pointer;
  }

  .nav-link:hover {
    background: #bebebe;
    color: #000;
  }

  .left-links .nav-link {
    float: left;
  }

  .right-links .nav-link {
    float: right;
  }
</style>

<div class={navbarClass}>
  <a href="https://amy-dickson.com">
    <div class="left-links">
      <div class="nav-link">Amy Dickson</div>
    </div>
  </a>
  <div class="right-links">
    <!-- <div class="nav-link">
      <i class="fa fa-file" />
      CV
    </div> -->
    <a href="#Portfolio">
      <div class="nav-link">
        <i class="fa fa-th" />
        Portfolio
      </div>
    </a>
    <!-- <div class="nav-link">
      <i class="fa fa-home" />
      Home
    </div> -->
  </div>
</div>
