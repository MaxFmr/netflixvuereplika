<template>
  <!-- Header -->
  <header id="header" class="bg-black flex">
    <nav class="">
      <!-- App Name -->
      <img
        src="../assets/logo.png"
        alt=""
        height="100"
        width="100"
        class="ml-2"
      />
      <div class="flex flex-grow items-center">
        <!-- Primary Navigation -->
        <!-- Navigation Links -->
        <!-- <ul class="flex flex-row mt-1">
          <li>
            <a class="px-2 text-white" href="#" @click.prevent="toggleAppModal"
              >Login / Register</a
            >
          </li>
          <li>
            <a class="px-2 text-white" href="#">Manage</a>
          </li>
        </ul> -->
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>
