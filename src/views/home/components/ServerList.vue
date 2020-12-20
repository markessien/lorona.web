<template>
  <ul class="grid grid-cols-1 gap-6 sm:grid-cols-1 lg:grid-cols-2">
    <li
      class="relative bg-white rounded-lg cursor-pointer group"
      v-for="(server, index) in servers"
      :key="index"
    >
      <div
        class="px-6 py-4 bg-white border border-l-8 border-green-600 rounded-lg "
      >
        <div class="flex items-center">
          <div class="text-sm">
            <p class="text-base font-semibold text-gray-900">
              {{ server.name }}
            </p>
            <p class="text-sm font-medium text-left text-green-600">
              Updated on {{ server.lastUpdated }}
            </p>
          </div>
        </div>
        <div class="mt-4 sm:flex sm:justify-between">
          <div class="flex items-center">
            <div class="text-sm">
              <p
                class="text-xs font-semibold text-left text-gray-500 uppercase"
              >
                CPU
              </p>
              <p
                class="mt-2 text-2xl font-bold leading-none text-left text-gray-700"
              >
                {{ server.cpu }}%
              </p>
            </div>
          </div>
          <div class="flex items-center">
            <div class="text-sm">
              <p
                class="text-xs font-semibold text-left text-gray-500 uppercase"
              >
                Temperature
              </p>
              <p
                class="mt-2 text-2xl font-bold leading-none text-left text-gray-700"
              >
                {{ server.temp }}<sup class="text-base">o</sup>C
              </p>
            </div>
          </div>
          <div class="flex items-center">
            <div class="text-sm">
              <p
                class="text-xs font-semibold text-left text-gray-500 uppercase"
              >
                Capacity
              </p>
              <p
                class="mt-2 text-2xl font-bold leading-none text-left text-gray-700"
              >
                {{ server.capacity }}
              </p>
            </div>
          </div>
          <div class="flex items-center">
            <div class="text-sm">
              <p
                class="text-xs font-semibold text-left text-gray-500 uppercase"
              >
                Powered ON
              </p>
              <p
                class="mt-2 text-2xl font-bold leading-none text-left text-gray-700"
              >
                {{ server.poweredOn }}
              </p>
            </div>
          </div>
        </div>
      </div>
      <div
        class="absolute inset-0 border-2 rounded-lg pointer-events-none hover:border-indigo-500"
        aria-hidden="true"
      ></div>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'ListItem',
  data() {
    return {};
  },
  props: {
    servers: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped></style>
