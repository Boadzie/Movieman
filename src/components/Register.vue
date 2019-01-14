<template>
  <v-container>
    <v-layout>
      <v-flex sm6 offset-md3>
        <v-card color="grey lighten-4 text-white">
          <v-form v-model="valid" ref="form" lazy-validation class="p-4">
            <v-text-field label="Name" v-model="name" required></v-text-field>
            <v-text-field label="Email" v-model="email" :rules="emailRules" required></v-text-field>
            <v-text-field label="Password" v-model="password" required></v-text-field>
            <v-text-field name="input-7-1" label="Confirm Password" v-model="confirm_password"></v-text-field>
            <v-btn @click="submit" :disabled="!valid">submit</v-btn>
            <v-btn @click="clear">clear</v-btn>
          </v-form>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>
