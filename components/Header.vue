<template>
  <!-- <nav class=" bg-gray-700 border-b border-gray-500 fixed inset-x-0 top-0 box-between text-white px-[10px] py-[5px]"> -->
  <header class=" bg-gray-700 border-b border-gray-500 fixed inset-x-0 top-0 px-[10px] py-[5px] grid grid-cols-4 gap-x-[20px]">
    <!-- Image & Search Box -->
    <HeaderLeftItems class="col-span-1" />

    <!-- btns -->
    <HeaderCenterItems class="col-span-2" />

    <!-- btns -->
    <HeaderRightItems class="col-span-1" />
  </header>
</template>

<script>
export default {
    name: 'DefaultHeader'
}
</script>