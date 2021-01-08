<template>
    <div class="sign-up-page">
        <h3>회원가입</h3>
        <signup-form @submit="onSubmit"/>
        <p>이미 가입하셨나요? <router-link :to="{name: 'Signup'}">로그인하러 가기</router-link></p>
    </div>
</template>

<script>
import SignupForm from '@/components/SignupForm';

export default{
  components: { SignupForm },
    name: 'Signup',
    componets: {
        SignupForm
    },
    methods:{
        onSubmit (payload) {
            console.log(payload);
        }
    }
}
</script>