<template>
  <v-container>
    <v-row justify="space-around">
      <v-card elevation="2" width="480" height="476">
        <form action="">
          <v-text-field
            v-model="email"
            outlined
            placeholder="Informe o email"
            label="exemplo@gmail.com"
          />
        </form>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'LoginPages'
}
</script>
