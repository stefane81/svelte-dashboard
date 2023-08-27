<script>
    import { page } from '$app/stores';
    import { Sidebar, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
    import { Icon } from 'flowbite-svelte-icons';
    $: activeUrl = $page.url.pathname;
    let activeClass = 'flex items-center p-2 text-base font-normal text-primary-900 bg-primary-200 dark:bg-primary-700 rounded-lg dark:text-white hover:bg-primary-100 dark:hover:bg-gray-700';
    let nonActiveClass = 'flex items-center p-2 text-base font-normal text-green-900 rounded-lg dark:text-white hover:bg-green-100 dark:hover:bg-green-700';
  </script>
  
  <Sidebar {activeUrl} {activeClass} {nonActiveClass}>
    <SidebarWrapper>
      <SidebarGroup>
        <SidebarItem label="Dashboard" href="/">
          <svelte:fragment slot="icon">
            <Icon name="chart-pie-solid" class="w-5 h-5" />
          </svelte:fragment>
        </SidebarItem>
        <SidebarItem label="Accordion" href="/docs/components/accordion">
          <svelte:fragment slot="icon">
            <Icon name="grid-solid" class="w-5 h-5" />
          </svelte:fragment>
        </SidebarItem>
        <SidebarItem label="Alert" href="/docs/components/alert">
          <svelte:fragment slot="icon">
            <Icon name="mail-box-solid" class="w-5 h-5" />
          </svelte:fragment>
        </SidebarItem>
        <SidebarItem label="Sidebar" href="/docs/components/sidebar">
          <svelte:fragment slot="icon">
            <Icon name="user-solid" class="w-5 h-5" />
          </svelte:fragment>
        </SidebarItem>
        <SidebarItem label="Badge" href="/docs/components/badge">
          <svelte:fragment slot="icon">
            <Icon name="arrow-right-to-bracket-solid" class="w-5 h-5" />
          </svelte:fragment>
        </SidebarItem>
      </SidebarGroup>
    </SidebarWrapper>
  </Sidebar>