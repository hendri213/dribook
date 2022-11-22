<template>
  <main class="bg-gray-900 min-h-screen text-white ">
      <Header />

    <section class="grid grid-cols-4 pt-[70px] gap-x-[20px]">
      <LeftSideNav />
      <Nuxt class="col-span-2" />
    </section>

  </main>
</template>

<script>
export default {
  name: 'DefaultLayout'
}
</script>