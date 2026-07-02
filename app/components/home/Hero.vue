<script setup lang="ts">
import heroUrl from '@/assets/images/hero.svg?url'

const { title, description } = useAppConfig()
</script>

<template>
  <section>
    <div
      class="
        py-16
        md:py-24
      "
    >
      <div
        class="
          mx-auto flex max-w-6xl flex-col items-center gap-12 px-6
          lg:flex-row lg:justify-between
        "
      >
        <div
          class="
            max-w-lg text-center
            lg:text-left
          "
        >
          <p
            class="
              mb-4 text-[11px] font-bold tracking-[0.18em] text-primary
              uppercase
            "
          >
            {{ description }}
          </p>

          <h1
            class="
              font-cal text-4xl leading-[0.9] font-extrabold -tracking-[0.04em]
              text-balance
              md:text-5xl
              xl:text-6xl
            "
          >
            {{ title }}
          </h1>
          <p class="mt-6 text-lg text-pretty text-muted-foreground">
            {{ description }}
          </p>

          <div
            class="
              mt-10 flex flex-col items-center justify-center gap-2
              sm:flex-row
              lg:justify-start
            "
          >
            <Button
              as-child
              size="lg"
              class="px-5 text-base"
            >
              <NuxtLink to="/dashboard">
                <span class="text-nowrap">{{ $t('dashboard.title') }}</span>
              </NuxtLink>
            </Button>
          </div>
        </div>

        <object
          type="image/svg+xml"
          :data="heroUrl"
          class="
            hidden aspect-square w-96 shrink-0
            md:block
            lg:w-[420px]
          "
          aria-label="Link sharing illustration"
          suppressHydrationWarning
        />
      </div>
    </div>
  </section>
</template>
