<template>
  <div id="app">
    <Sidebar />
    <section id="interface">
      <Navbar />
      <h3 class="i-name"></h3>
      <UserStats @openAddUserPopup="openAddUserModal" />
      <UserTable @openEditUserPopup="openEditUserModal" />
      <EditUserModal 
      :user="selectedUser"
      :isVisible="isEditUserModalVisible"
      @closeModal="closeEditUserModal"
      @saveChanges="handleSaveChanges"
      />
      <AddUserModal 
      v-if="isAddUserModalVisible"
      :isAddUserModalVisible="isAddUserModalVisible"
      @closeModal="closeAddUserModal"
      @addUser="handleAddUser"
      />
    </section>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue';
import Navbar from './components/Navbar.vue';
import UserStats from './components/UserStats.vue';
import UserTable from './components/UserTable.vue';
import EditUserModal from './components/EditUserModal.vue';
import AddUserModal from './components/AddUserModal.vue';

export default {
  components: {
    Sidebar,
    Navbar,
    UserStats,
    UserTable,
    EditUserModal,
    AddUserModal,
  },
  data() {
    return {
      isAddUserModalVisible: false,
      isEditUserModalVisible: false,
      selectedUser: null,
      isModalVisible: false,
      
    };
  },
  methods: {
    openAddUserModal() {
      console.log('Add User Popup Triggered');
      this.isAddUserModalVisible = true;
    },
    closeAddUserModal() {
      this.isAddUserModalVisible = false;
    },
    openEditUserModal(user) {
      console.log('Editing user:', user);
      this.selectedUser = user;
      this.isEditUserModalVisible = true;
    },
    closeEditUserModal() {
      this.isEditUserModalVisible = false;
      this.selectedUser = null;
    },
    handleAddUser(newUser) {
      console.log('New user added:', newUser);
      this.closeAddUserModal();
    },
    handleSaveChanges(updatedUser) {
      console.log('User updated:', updatedUser);
      this.closeEditUserModal();
    },
    closeModal() {
      this.isModalVisible = false;
    },
    saveChanges(updatedUser) {
      console.log('User saved:', updatedUser);
      this.isModalVisible = false;
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

body {
  width: 100%;
  background: rgb(223, 222, 222);
  position: relative;
  display: flex;
}

#interface {
  width: 100%;
  margin-left: 100px;
  position: relative;
}


</style>