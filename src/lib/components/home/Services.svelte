<script lang="ts">
  const services = [
    {
      title: 'SME Software Development',
      description: 'Custom software solutions tailored to your business needs',
      icon: '💻'
    },
    {
      title: 'Process Automation',
      description: 'Streamline your operations with intelligent automation',
      icon: '⚡'
    },
    {
      title: 'AI Solutions',
      description: 'Leverage artificial intelligence for smarter decision-making',
      icon: '🤖'
    },
    {
      title: 'Research Services',
      description: 'Data-driven insights to power your business strategy',
      icon: '📊'
    },
    {
      title: 'Administrative Services',
      description: 'Efficient management of your business processes',
      icon: '📋'
    },
    {
      title: 'Integration Services',
      description: 'Seamless connection of your business systems',
      icon: '🔄'
    }
  ] as const;
</script>

<section class="py-20 bg-gray-50 dark:bg-gray-800">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <h2 class="text-3xl font-heading font-bold text-center mb-12 text-gray-900 dark:text-white">
      Our Services
    </h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each services as service}
        <div class="bg-white dark:bg-gray-900 p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow">
          <div class="text-4xl mb-4">{service.icon}</div>
          <h3 class="text-xl font-heading font-semibold mb-2 text-gray-900 dark:text-white">
            {service.title}
          </h3>
          <p class="text-gray-600 dark:text-gray-300">
            {service.description}
          </p>
        </div>
      {/each}
    </div>
  </div>
</section>