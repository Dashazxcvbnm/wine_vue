<template>
<div>
    <form 
    class="form">

        <div class="input-wrapper">
            <WineVueInput 
            class="input_top" 
            type="text"
            placeholder="Имя"
            v-model="name"
            @input="validateName"
            :class="{'error-input': !nameValid}"/>

            <span
            class="error-field error-field_name" 
            v-if="!nameValid">{{ errorName }}</span>

            <WineVueInput 
            class="input_top"
            type="tel"
            placeholder="Телефон"
            v-model="phone"
            @input="validatePhone"
            :class="{'error-input': !phoneValid}"/>

            <span
            class="error-field error-field_phone" 
            v-if="!phoneValid">{{ errorPhone }}</span>
        </div>

        <WineVueInput 
        class="input_bottom"
        type="text"
        placeholder="Бутик на Невском 103"
        v-model="add"
        @input="validateAdd"
        :class="{'error-input': !addValid}"/>

        <span
        class="error-field error-field_add" 
        v-if="!addValid">{{ errorAdd }}</span>

        <button 
        class="button"
        type="sumbmit"
        @click.prevent="!checkForm">
        записаться
        </button>

    </form>

    <div class="modal-window">
        <span>Форма отправлена</span>
    </div>

</div>
</template>

<script setup>
import WineVueInput from './GUI/WineVueInput.vue';
import { ref, computed } from 'vue'

const errorName = ref('')
const errorPhone = ref('')
const errorAdd = ref('')

const Validator = {

  validateName(name) {
    const minLength = 2;
    const regex = /[А-Я][а-я]+/g;
   
    if (!name.length) {
        errorName.value = 'Заполните поле'
        return false
    }
    if (!regex.test(name) || name.length <= minLength) {
        errorName.value = 'Имя некорректно';
        return false
    }
        return !!name
  },

  validatePhone(phone) {
    const regex = /^[8][0-9]{10}$/;

    if (!phone.length) {
        errorPhone.value = 'Заполните поле'
        return false
    }
    if (!regex.test(phone)) {
        errorPhone.value = 'Телефон некорректный';
        return false
    }
        return !!phone
},

  validateAdd(add) {
    if (!add.length) {
        errorAdd.value = 'Заполните поле'
        return false
    }
        return !!add
  }

};

const name = ref('')
const phone = ref('')
const add = ref('')

const nameValid = ref(false)
const phoneValid = ref(false)
const addValid = ref(false)

function validateName() {
    nameValid.value = Validator.validateName(name.value);
 }

function validatePhone() {
    phoneValid.value = Validator.validatePhone(phone.value);
 }

 function validateAdd() {
    addValid.value = Validator.validateAdd(add.value);
 }

 const checkForm = computed(() => {
 const formValid = nameValid.value && phoneValid.value && addValid.value;
      if (formValid) {
        document.querySelector('.form').reset();
        const successModal = document.querySelector('.modal-window');
        successModal.style.display = 'block';

          setTimeout(()=> {
                successModal.style.display = 'none'
            }, 5000)
      }
      })
  
</script>

<style scoped>

.form {
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: space-between;
    padding-top: 15px;
}

.button {
    width: 100%;
    border: 1px solid rgb(255, 255, 255);
    background: #282828;
    color: #ffffff;
    padding: 15px;
    font-size: 16px;
    line-height: 20px;
    font-family: 'Montserrat';
    text-transform: uppercase;
    cursor: pointer;
    white-space: nowrap;
}

.input-wrapper {
    display: flex;
    justify-content: space-between;
}

.input_top {
    width: 47%;
}

.input_bottom {
    width: 100%;
}

.error-field {
    position: absolute;
    display: block;
    color: #ff0000;
    font-size: 13px;
}

.error-field_name {
    transform: translate(0px, 35px);
}

.error-field_phone {
    transform: translate(285px, 35px);
}

.error-field_add {
    transform: translate(0px, 108px);
}

.error-input {
    border-bottom: 1px solid #ff0000;
}

.error-input:focus {
    border-bottom: 1px solid #ffffff;
}

.modal-window {
    position:  absolute;
    width: 250px;
    height: 50px;
    background-color: #696969;
    display: none;
    transform: translate(150px, -250px);
    text-align: center;
}
</style>