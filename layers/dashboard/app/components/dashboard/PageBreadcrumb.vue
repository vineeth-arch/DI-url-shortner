<script setup lang="ts">
defineProps<{
  title: string
}>()
</script>

<template>
  <Breadcrumb>
    <BreadcrumbList>
      <BreadcrumbItem>
        <span class="text-muted-foreground">
          {{ $t('dashboard.title') }}
        </span>
      </BreadcrumbItem>
      <BreadcrumbSeparator />
      <BreadcrumbItem>
        <BreadcrumbPage
          class="font-cal leading-[0.95] font-extrabold -tracking-[0.02em]"
        >
          {{ title }}
        </BreadcrumbPage>
      </BreadcrumbItem>
    </BreadcrumbList>
  </Breadcrumb>
</template>
