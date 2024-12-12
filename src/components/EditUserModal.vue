<template>
    <div v-if="isVisible" class="modal" @click.self="closePopup">
      <div class="modal-content">
        <!-- User Picture -->
        <div v-if="modalPicture" class="user-picture">
          <img :src="modalPicture" alt="User Picture" />
        </div>
  
        <form @submit.prevent="saveChanges">
          <!-- Name -->
          <input 
            v-model="modalName" 
            id="modalName" 
            placeholder="Name" 
          />
  
          <!-- Date of Birth -->
          <input 
            v-model="modalDOB" 
            type="date" 
            id="modalDOB" 
          />
  
          <!-- Phone -->
          <input 
            v-model="modalPhone" 
            id="modalPhone" 
            placeholder="Phone" 
          />
  
          <!-- Email -->
          <input 
            v-model="modalEmail" 
            id="modalEmail" 
            placeholder="Email" 
          />
  
          <!-- Gender -->
          <div class="radio-group">
            <label>
              <input 
                type="radio" 
                value="Female" 
                v-model="modalGender" 
              /> Female
            </label>
            <label>
              <input 
                type="radio" 
                value="Male" 
                v-model="modalGender" 
              /> Male
            </label>
          </div>
  
          <!-- Status -->
          <div class="radio-group">
            <label>
              <input 
                type="radio" 
                value="Active" 
                v-model="modalStatus" 
              /> Active
            </label>
            <label>
              <input 
                type="radio" 
                value="Inactive" 
                v-model="modalStatus" 
              /> Inactive
            </label>
          </div>
  
          <!-- Buttons -->
          <div class="button-group">
            <button type="submit">Save Changes</button>
            <button type="submit">Delete</button>
            <button type="button" @click="closePopup">Close</button>
          </div>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      user: {
        type: Object,
        default: null,
      },
      isVisible: {
        type: Boolean,
        default: false,
      },
    },
    data() {
      return {
        modalName: '',
        modalDOB: '',
        modalPhone: '',
        modalEmail: '',
        modalGender: '',
        modalStatus: '',
        modalPicture: '', // Store the user's picture URL
      };
    },
    watch: {
      user: {
        immediate: true,
        handler(newUser) {
          if (newUser) {
            this.modalName = newUser.name || '';
            this.modalDOB = newUser.dob || '';
            this.modalPhone = newUser.phone || '';
            this.modalEmail = newUser.email || '';
            this.modalGender = newUser.gender || '';
            this.modalStatus = newUser.status || '';
            this.modalPicture = newUser.picture || ''; // Bind the picture URL
          }
        },
      },
    },
    methods: {
      saveChanges() {
        const updatedUser = {
          name: this.modalName,
          dob: this.modalDOB,
          phone: this.modalPhone,
          email: this.modalEmail,
          gender: this.modalGender,
          status: this.modalStatus,
        };
        this.$emit('saveChanges', updatedUser);
        this.closePopup();
      },
      closePopup() {
        this.$emit('closeModal');
      },
      deleteUser() {
      this.$emit('deleteUser', this.newUser);
      this.closeAddUserPopup(); // Close modal after deleting
    },
    },
  };
  </script>
  
  <style scoped>
  .modal {
    display: flex;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    justify-content: center;
    align-items: center;
  }
  
  .modal-content {
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    width: 40%;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    position: relative;
    text-align: left;
  }
  
  .user-picture img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 10px;
  }
  
  input {
    width: calc(100% - 20px);
    padding: 8px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 14px;
  }
  
  .radio-group {
    margin-bottom: 10px;
    display: flex;
    gap: 15px;
  }
  
  button {
    padding: 10px 15px;
    margin-top: 10px;
    border: none;
    border-radius: 5px;
    background-color: #007bff;
    color: white;
    font-size: 14px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  button:active {
    transform: scale(0.98);
  }
  
  .button-group {
    display: flex;
    gap: 10px;
  }
  </style>
  