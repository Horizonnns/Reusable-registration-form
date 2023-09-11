<template>
  <section class="flex justify-center items-center py-10">
    <div>
      <h1 class="text-3xl font-bold text-center mb-6">Registration Form</h1>

      <form class="w-full max-w-xs space-y-5">
        <!-- name -->
        <div class="space-y-1">
          <label for="name">Name <span class="text-red-500">*</span></label>
          <input
            type="text"
            id="name"
            placeholder="Mike Mke"
            class="w-full border rounded-sm text-sm px-2.5 py-1.5"
          />
        </div>

        <!-- email -->
        <div class="space-y-1">
          <label for="email">Email <span class="text-red-500">*</span></label>
          <input
            type="text"
            id="email"
            placeholder="kasim@mail.ru"
            class="w-full border rounded-sm text-sm px-2.5 py-1.5"
          />
        </div>

        <!-- password -->
        <div class="space-y-1">
          <label for="password"
            >Password <span class="text-red-500">*</span></label
          >
          <input
            type="password"
            id="password"
            placeholder="*********"
            class="w-full border rounded-sm text-sm px-2.5 py-1.5"
          />
        </div>

        <button
          class="bg-blue-600 hover:bg-blue-700 active:bg-blue-500 text-white duration-150 w-full px-10 py-2"
        >
          Register
        </button>
      </form>
    </div>
  </section>
</template>
