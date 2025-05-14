<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="flex w-full h-fit justify-center items-center border-[rgba(0,0,0,0.1)] border-t p-[60px] gap-x-[70px]">
        <div class=" flex flex-col gap-y-[20px] text-left w-[500px]">
            <h class="font-Poppins font-semibold text-[40px]">
                Contact us
            </h>
            <h class=" font-Roboto text-[16px]">
                Have a question or need assistance? Reach out to us.
            </h>
        </div>
        <div class="flex flex-col gap-y-[25px]">
            <ContactField :type="'text'" :FieldName="'Name'" :placeholder="'Enter your name'"/>
            <ContactField :type="'email'" :FieldName="'Email'" :placeholder="'Enter your email'"/>
            <ContactField :type="'textarea'" :FieldName="'Message'" :placeholder="'Enter your message'"/>
            <span
            class="cursor-pointer p-[12px] w-[240px] text-center items-center justify-center rounded-[10px] font-semibold text-white bg-[#713D86] transition-all duration-300 ease-in-out hover:scale-105 hover:shadow-[0px_1px_12px_4px_rgba(0,_0,_0,_0.1)] self-center">
            Submit
            </span>
        </div>
    </div>
</template>

<script setup lang="ts">
import ContactField from './ContactField.vue';
</script>
