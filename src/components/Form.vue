<script setup>
import { ref } from 'vue';
import Label from './Label.vue';
import Input from './Input.vue';
import ErrorMessage from './ErrorMessage.vue';
import HelperMessage from './HelperMessage.vue';

const errors = ref({
  name: 'Имя не запонено!',
  email: 'Email не запонено!',
  password: 'Password не заполнено!',
});

const form = ref({
  name: '',
  email: '',
  password: '',
});
</script>

<template>
  <section class="flex justify-center items-center py-10">
    <div>
      <h1 class="text-3xl font-bold text-center mb-6">Registration Form</h1>

      <form class="w-full max-w-md space-y-4 p-4">
        <!-- name -->
        <div class="space-y-1">
          <Label for="name" required>Name</Label>

          <Input
            id="name"
            type="text"
            v-model="form.name"
            placeholder="Mike Mke"
            :invalid="!!errors.name"
          />

          <ErrorMessage v-if="errors.name">
            {{ errors.name }}
          </ErrorMessage>
        </div>

        <!-- email -->
        <div class="space-y-1">
          <Label for="email" required>Email</Label>

          <Input
            id="email"
            type="text"
            v-model="form.email"
            placeholder="kasim@mail.ru"
            :invalid="!!errors.email"
          />

          <ErrorMessage v-if="errors.email">
            {{ errors.email }}
          </ErrorMessage>
        </div>

        <!-- password -->
        <div class="space-y-1">
          <Label for="password" required>Password</Label>

          <Input
            id="password"
            type="password"
            v-model="form.password"
            placeholder="*********"
            :invalid="!!errors.password"
          />

          <ErrorMessage v-if="errors.password">
            {{ errors.password }}
          </ErrorMessage>

          <HelperMessage id="help-password">
            Should be at least 8 characters long.
          </HelperMessage>
        </div>

        <button
          class="bg-blue-600 hover:bg-blue-700 active:bg-blue-500 text-white duration-150 rounded-sm w-full px-10 py-2"
        >
          Register
        </button>
      </form>
    </div>
  </section>
</template>
