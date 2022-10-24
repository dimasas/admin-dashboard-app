<template>
    <v-app class="bg-mainApp">
      <v-container bg fill-height>
        <v-row no-gutters>
          <v-col md="6" align-center>
            ...
          </v-col>
          <v-col md="6" align-center>
            <!-- Panel Card  -->
              <v-card tile elevation="2" class="rounded-lg mt-10 px-3 py-3">
                  <v-card-title>
                      <h3>Login Admin</h3>
                  </v-card-title>
                  <v-form @submit.prevent="handleSubmitLogin">
                  <v-card-text>
                          <v-text-field label="Email" prepend-icon="mdi-account-circle" v-model="user.email" :rules="emailRules"/>
                          <v-text-field label="Password" prepend-icon="mdi-lock" 
                            :type="showPassword ? 'text' : 'password'" 
                            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                            @click:append="handleClick"
                            v-model="user.password" 
                            :rules="passwordRules"/>
                  </v-card-text>
                  <v-card-actions>
                      <v-btn color="success" v-on:click="handleSubmitLogin">Login</v-btn>
                      <v-btn color="info">Register</v-btn>
                  </v-card-actions>                
                </v-form>
              </v-card>
            <!-- ./end:Panel Card -->
          </v-col>
        </v-row> 
      </v-container>
    </v-app>
  </template>
  <script>
  export default{
    name:'App',
    data(){
      return{
        showPassword:false,
        // object user
        user:{
          email:'',
          password:'',
        },
        // rules validation
        emailRules: [
          v => !!v || 'E-mail is required',
          v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
        ],
        passwordRules: [
          v => !!v || 'Password is required',
          v => v.length >= 8 || 'Password must be at least 8 characters',
        ],
      }
    },
    methods:{
      handleClick(){
        this.showPassword = !this.showPassword
      },
      handleSubmitLogin(){
        console.log(this.user)
        this.user={
          email:'',
          password:'',
        }
      }
    }
  }
  </script>
  
  <style>
  </style>