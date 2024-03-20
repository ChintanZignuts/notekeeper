<script setup lang="ts">
const formdata = ref({
  name: "",
  email: "",
  password: "",
  confirmPassword: "",
});
</script>
<template>
  <VContainer class="d-flex align-center justify-center h-100">
    <VCard title="User Login" class="w-100 pa-8" max-width="600">
      <VContainer>
        <VRow>
          <VCol cols="12">
            <VTextField
              v-model="formdata.name"
              variant="outlined"
              label="Name"
              required
            ></VTextField>
          </VCol>
          <VCol cols="12">
            <VTextField
              v-model="formdata.email"
              variant="outlined"
              label="Email"
              required
            ></VTextField>
          </VCol>
          <VCol cols="12">
            <VTextField
              v-model="formdata.password"
              variant="outlined"
              label="Password"
              required
            ></VTextField>
          </VCol>
          <VCol cols="12">
            <VTextField
              v-model="formdata.confirmPassword"
              variant="outlined"
              label="Confirm Password"
              required
            ></VTextField>
          </VCol>
          <VCol cols="12">
            <VBtn
              size="x-large"
              type="submit"
              color="blue-grey"
              class="text-none"
              block
            >
              Sign Up
            </VBtn>
          </VCol>
          <VDivider></VDivider>
          <VCol cols="12" class="text-center">
            <p>
              Already have an account?
              <NuxtLink to="/signin"> Sign In </NuxtLink>
            </p>
          </VCol>
        </VRow>
      </VContainer>
    </VCard>
  </VContainer>
</template>
