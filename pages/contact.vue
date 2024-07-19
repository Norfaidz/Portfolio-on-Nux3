<template>
    <div class="contact-container">
        <div class="contact-info">
            <h2>Contact me</h2>
            <h3>Let's <span>Connect</span> here</h3>
            <ul>
                <li>
                    <img src="/assets/icons/call.png" alt="Phone Icon">
                    <p>+63 935-674-3879</p>
                </li>
                <li>
                    <a href="https://mail.google.com/mail/u/0/#inbox?compose=DmwnWrRmVXGTzMggTbxwmCHdhMRRBhzZhbGphKrDgMDPKDqnKksjjxQNWhprmplhXMWWkWpljJcL" target="_blank">
                        <img src="/assets/icons/email.png" alt="Email Icon">
                        <p style="color: #f3fbfb;">inorfaidz@gmail.com</p>
                    </a>
                </li>
                <li>
                    <a href="https://maps.app.goo.gl/uXqmvHxozwCoFKbe9" target="_blank">
                        <img src="/assets/icons/location-pin.png" alt="Location Icon">
                        <p style="color: #f3fbfb;">Zone 7, Bulua, Cagayan de Oro City, Misamis Oriental</p>
                    </a>
                </li>
            </ul>
            <div class="social-icons">
                <a href="" target="_blank"><img src="/assets/icons/facebook-app-symbol.png" alt="Facebook"></a>
                <a href="https://www.instagram.com/aym_faidz/" target="_blank"><img src="/assets/icons/instagram.png" alt="Instagram"></a>
                <a href="https://github.com/Norfaidz" target="_blank"><img src="/assets/icons/github.png" alt="Github"></a>
            </div>
        </div>
        <div class="contact-form">
            <form @submit.prevent="handleSubmit">
                <label for="name">Name:</label>
                <input type="text" v-model="name" id="name" name="name" placeholder="Ex. Daniel Padilla">
                
                <label for="email">Email:</label>
                <input type="email" v-model="email" id="email" name="email" placeholder="sample@gmail.com">
                
                <label for="message">Message:</label>
                <textarea v-model="message" id="message" name="message" placeholder="Enter here..."></textarea>
                
                <button type="submit">Submit</button>
            </form>
            <p v-if="formMessage" :style="{ color: messageColor }">{{ formMessage }}</p>
        </div>
    </div>
</template>


<script setup>
import { ref } from 'vue';

const name = ref('');
const email = ref('');
const message = ref('');
const formMessage = ref('');
const messageColor = ref('red');

const handleSubmit = () => {
    if (name.value === '' || email.value === '' || message.value === '') {
        formMessage.value = 'Please fill in all fields.';
        messageColor.value = 'red';
    } else {
        formMessage.value = 'Thank you for your message!';
        messageColor.value = 'green';
        // Reset the form fields
        name.value = '';
        email.value = '';
        message.value = '';
    }
};
</script>
