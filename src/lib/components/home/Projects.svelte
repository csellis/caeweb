<script lang="ts">
  const projects = [
    {
      title: 'ERP System Integration',
      description: 'Custom ERP solution for manufacturing company',
      image: '/images/project1.jpg'
    },
    {
      title: 'AI-Powered Analytics',
      description: 'Predictive analytics platform for retail',
      image: '/images/project2.jpg'
    },
    {
      title: 'Process Automation Suite',
      description: 'Automated workflow system for healthcare',
      image: '/images/project3.jpg'
    }
  ];
</script>

<section class="py-20">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <h2 class="text-3xl font-heading font-bold text-center mb-12 text-gray-900 dark:text-white">
      Recent Projects
    </h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      {#each projects as project}
        <div class="bg-white dark:bg-gray-900 rounded-lg overflow-hidden shadow-lg">
          <div class="h-48 bg-gray-200 dark:bg-gray-700"></div>
          <div class="p-6">
            <h3 class="text-xl font-heading font-semibold mb-2 text-gray-900 dark:text-white">
              {project.title}
            </h3>
            <p class="text-gray-600 dark:text-gray-300">
              {project.description}
            </p>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>