<template>
  <div
    class="bg-gray-800 text-gray-100 py-3.5 px-6 shadow md:flex justifiy-between items-center"
  >
    <div class="flex items-center cursor-pointer">
      <span class="text-green-500 text-xl mr-1">
        <i class="bi bi-messenger"></i>
      </span>

      <h1 class="text-xl">
        <img src="https://www.mintyhost.com/wp-content/uploads/2023/06/mintyhost-logotipo.svg" alt="Minty Host Logo" class="h-8 w-auto mr-2">
        Minty Host
      </h1>
    </div>

    <span
      @click="MenuOpen()"
      class="absolute md:hidden right-6 top-1.5 cursor-pointer text-4xl"
    >
      <i :class="[open ? 'bi bi-x' : 'bi bi-filte-left']"></i>
    </span>

    <ul
      class="md:flex md:items-center md:px-0 px-10 md:pb-0 pb-10 md:static absolute bg-gray-900 md:w-auto w-full top-14 duration-700 ease-in"
      :class="[open ? 'left-0' : 'left-[-100%]']">
      <li class="md:mx-4 md:my-0 my-6" v-for="link in Links">
        <a href="link.link" class="text-xl hover:text-green-500">{{link.name}}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  setup() {
    let Links = [
      {
        name: "Viviendas",
        link: "#",
      },
      {
        name: "Contactos",
        link: "#",
      },
      {
        name: "Preguntas",
        link: "#",
      },
    ];
    return { Links };
  },
};
</script>
