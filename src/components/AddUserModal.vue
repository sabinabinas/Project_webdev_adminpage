<template>
    <div>
      <!-- Add User Modal -->
      <div v-if="isAddUserModalVisible" class="modal" id="addUserModal">
        <div class="modal-content">
          <span class="close" @click="closeAddUserPopup">&times;</span>
          <h3>Add New User</h3>
          <form @submit.prevent="saveNewUser">
            <!-- Name -->
            <input 
              v-model="newUser.name" 
              placeholder="Name" 
              required 
            />
            <!-- Date of Birth -->
            <input 
              v-model="newUser.dob" 
              type="date" 
              required 
            />
            <!-- Phone -->
            <input 
              v-model="newUser.phone" 
              placeholder="Phone" 
              required 
            />
            <!-- Email -->
            <input 
              v-model="newUser.email" 
              type="email" 
              placeholder="Email" 
              required 
            />
            <!-- Gender -->
            <div class="radio-group">
              <label>
                <input 
                  type="radio" 
                  id="genderFemale" 
                  value="Female" 
                  v-model="newUser.gender" 
                /> Female
              </label>
              <label>
                <input 
                  type="radio" 
                  id="genderMale" 
                  value="Male" 
                  v-model="newUser.gender" 
                /> Male
              </label>
            </div>
            <!-- Buttons -->
            <div class="button-group">
              <button type="submit">Save New User</button>
              <button type="button" @click="closeAddUserPopup">Close</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: ['isAddUserModalVisible'],
    data() {
      return {
        newUser: {
          name: '',
          dob: '',
          phone: '',
          email: '',
          gender: '',
        },
      };
    },
    methods: {
      closeAddUserPopup() {
        this.$emit('closeModal'); // Emit event to close the modal in parent
      },
      saveNewUser() {
        // Collect data and send it to the parent component
        this.$emit('addUser', this.newUser);
        this.closeAddUserPopup(); // Close modal after saving
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
  
  .close {
    position: absolute;
    top: 10px;
    right: 15px;
    font-size: 24px;
    cursor: pointer;
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
  