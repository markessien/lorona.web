<template>
  <div>
    <div class="relative pb-32 overflow-hidden bg-light-blue-700">
      <div
        class="absolute inset-x-0 flex justify-center w-full overflow-hidden transform -translate-x-1/2 left-1/2 lg:inset-y-0"
        aria-hidden="true"
      >
        <div class="flex-grow bg-opacity-75 bg-light-blue-900"></div>
        <svg
          class="flex-shrink-0"
          width="1750"
          height="308"
          viewBox="0 0 1750 308"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            opacity=".75"
            d="M1465.84 308L16.816 0H1750v308h-284.16z"
            fill="#075985"
          />
          <path
            opacity=".75"
            d="M1733.19 0L284.161 308H0V0h1733.19z"
            fill="#0c4a6e"
          />
        </svg>
        <div class="flex-grow bg-opacity-75 bg-light-blue-800"></div>
      </div>
      <header class="relative py-10">
        <div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
          <h1 class="text-3xl font-bold text-white">
            Dashboard
          </h1>
        </div>
      </header>
    </div>

    <main class="relative -mt-32">
      <div class="max-w-screen-xl px-4 pb-6 mx-auto sm:px-6 lg:pb-16 lg:px-8">
        <div class="p-5 overflow-hidden bg-white rounded-lg">
          <ServerList :servers="servers" />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import ServerList from './components/ServerList';
export default {
  name: 'Dashboard',
  components: {
    ServerList,
  },
  data() {
    return {
      servers: [
        {
          name: 'HNG Core',
          cpu: '45',
          temp: '37',
          capacity: '465.8 GB',
          lastUpdated: 'August 18, 2020',
          poweredOn: '1.6 years',
        },
        {
          name: 'HNG DB',
          cpu: '20',
          temp: '31',
          capacity: '12.73 TB',
          lastUpdated: 'August 18, 2020',
          poweredOn: '131.3 days',
        },
        {
          name: 'HNG Apps',
          cpu: '50',
          temp: '31',
          capacity: '12.73 TB',
          lastUpdated: 'August 18, 2020',
          poweredOn: '131.3 days',
        },
        {
          name: 'HNG WorkHorse',
          cpu: '12',
          temp: '30',
          capacity: '7.28 TB',
          lastUpdated: 'August 18, 2020',
          poweredOn: '2.9 years',
        },
        {
          name: 'HNG LoadBalancer',
          cpu: '30',
          temp: '29',
          capacity: '12.73 TB',
          lastUpdated: 'August 18, 2020',
          poweredOn: '131.3 days',
        },
        {
          name: 'HNG Images',
          cpu: '15',
          temp: '29',
          capacity: '12.73 TB',
          lastUpdated: 'August 18, 2020',
          poweredOn: '5.4 years',
        },
        {
          name: 'HNG Videos',
          cpu: '30',
          temp: '37',
          capacity: '495.8 GB',
          lastUpdated: 'August 20, 2020',
          poweredOn: '1 year',
        },
        {
          name: 'HNG Maps',
          cpu: '40',
          temp: '30',
          capacity: '7.28 TB',
          lastUpdated: 'August 18, 2020',
          poweredOn: '2.9 years',
        },
      ],
    };
  },
};
</script>

<style scoped></style>
