<template>
<div>
    <form 
    class="form">

        <div class="input-wrapper">
            <WineVueInput 
            class="input input_top" 
            type="text"
            placeholder="Имя"
            v-model="input.name"
            required/>

            <span
            class="error-field error-field_name" 
            v-if="!nameValid">{{ errorName }}</span>

            <WineVueInput 
            class="input input_top"
            type="tel"
            placeholder="Телефон"
            v-model="input.phone"
            required/>

            <span
            class="error-field error-field_phone" 
            v-if="!phoneValid">{{ errorPhone }}</span>
        </div>

        <WineVueInput 
        class="input input_bottom"
        type="text"
        placeholder="Бутик на Невском 103"
        v-model="input.add"
        required/>

        <span
        class="error-field error-field_add" 
        v-if="!addValid">{{ errorAdd }}</span>

        <button 
        class="button"
        @click.prevent="checkForm">
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
import { reactive, ref, computed } from 'vue'


const input = reactive({
  name: '',
  phone: '',
  add: ''
})

const errorName = ref('')
const errorPhone = ref('')
const errorAdd = ref('')

const nameValid = computed(() => {
    const value = input.name
    if (!value.length) {
        errorName.value = 'Заполните поле'
        return false
    }
    
    if (!(/[А-Я][а-я]+/g.test(value)) || (value.length <= 2)) {
        errorName.value = 'Имя некорректно';
        return false
    }
    errorName.value = ''
        return !!value
})

const phoneValid = computed(() => {
    const value = input.phone
    const globalRegex = new RegExp('^[8][0-9]{10}$');
    if (!value.length) {
        errorPhone.value = 'Заполните поле'
        return false
    }
    
    if (!globalRegex.test(value)) {
        errorPhone.value = 'Телефон некорректный';
        return false
    }
        return !!value
})

const addValid = computed(() => {
    const value = input.add
    if (!value.length) {
        errorAdd.value = 'Заполните поле'
        return false
    }
        return !!value
})


function checkForm() {
    const formValid = nameValid.value && phoneValid.value && addValid.value
      if (formValid) {
        document.querySelector('.form').reset();
        const successModal = document.querySelector('.modal-window');
        successModal.style.display = 'block';

            setTimeout(()=> {
                successModal.style.display = 'none'
            }, 5000)
            
      }
      return
    }
  
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

.input:valid {
    border-bottom: 1px solid #ffffff;
}

.input:invalid {
    border-bottom: 1px solid #ff0000;
}

.input:focus {
    border-bottom: 1px solid #ffffff;
}

.modal-window {
    position:  absolute;
    width: 250px;
    height: 50px;
    background-color: rgb(105, 105, 105);
    display: none;
    transform: translate(150px, -250px);
    text-align: center;
}
</style>