<template>
  <nav class="uk-navbar-container" uk-navbar>
    <div class="uk-navbar-left">
      <ul class="uk-navbar-nav">
        <li class="uk-active"><a href="#">FA</a></li>
      </ul>
    </div>
    <div class="uk-navbar-center">
      <ul class="uk-navbar-nav">
        <li class="uk-active"><a href="#">About Me</a></li>
        <li>
          <a href="#">Portfolio</a>
          <div class="uk-navbar-dropdown">
            <ul class="uk-nav uk-navbar-dropdown-nav">
              <li class="uk-active"><a href="#">Active</a></li>
              <li><a href="#">Item</a></li>
              <li><a href="#">Item</a></li>
            </ul>
          </div>
        </li>
        <li><a href="#">Item</a></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  
}
</script>

<style>
nav {
  padding: 0px 80px;
}
</style>