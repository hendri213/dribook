<template>
  <!-- <div class="relative"> -->
    <div class="px-[10px]">
      <NuxtLink
        to="/profile"
        class="box-equal p-[10px] gap-x-[10px] hover:bg-gray-600 w-full rounded-lg"
      >

      <!-- img -->
      <div
       class="w-[24px] h-[24px] min-w-[24px] min-h-[24px] max-w-[24px] max-h-[24px] rounded-full"
      :style="{backgroundImage: 'url(https://picsum.photos/40)'}"
      />

      <!-- text -->
      Hendri

      </NuxtLink>

      <NuxtLink
        v-for="link1 in links1"
        :key="'left-sidenav-link-' + link1.icon"
        :to="link1.url"
        class="box-equal p-[10px] gap-[5px]  hover:bg-gray-600 w-full rounded-lg"
      >
          <!-- icon -->
          <client-only>
            <unicon :name="link1.icon" fill="white" />
          </client-only>

        <!-- text -->
        {{ link1.text }}
      </NuxtLink>

      <hr class="border-t border-gray-700 mb-[10px]" />

      <!-- footer text-->
      <div class="text-sm">
        <NuxtLink to="#">Privasi</NuxtLink>
        &middot;
        <NuxtLink to="#">Ketentuan</NuxtLink>
        &middot;
        <NuxtLink to="#">Lainnya</NuxtLink>
        &middot;
        <NuxtLink to="#">Mabook &copy; {{ currentYear }}</NuxtLink>
      </div>
    </div>
  <!-- </div> -->
</template>

<script>
const links1 = [
  {url: '#', icon: 'user', text: 'Teman'},
  {url: '#', icon: 'users-alt', text: 'Grup'},
  {url: '#', icon: 'store', text: 'Marketplace'},
  {url: '#', icon: 'video', text: 'Watch'},
]

export default {
  data() {
    return {
       links1,
    }
  },
  computed: {
    currentYear() {
      return new Date().getFullYear()
    }
  }
}
</script>