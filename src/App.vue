<script setup lang="ts">
import Sidebar from '@/components/Sidebar.vue';
import Navbar from '@/components/Navbar.vue';
import UserStats from '@/components/UserStats.vue';
import UserTable from '@/components/UserTable.vue';
import EditUserModal from '@/components/Modals/EditUserModal.vue';
import AddUserModal from '@/components/Modals/AddUserModal.vue';
import { ref } from 'vue';
import { User } from '@/types/User';
import { users } from '@/data/users';

const addUser = ref(false)
const editUser = ref(false)
const selectedUser = ref({} as User)

function openEditUserModal(user: User) {
  console.log('Editing user:', user);
  selectedUser.value = user;
  editUser.value = true;
}

</script>

<template>
  <Sidebar />
  <main>
    <section id="interface" class="content">
      <Navbar />
      <h3 class="title">User Management</h3>
      <UserStats @openAddUserPopup="addUser = true" />
      <UserTable @openEditUserPopup="openEditUserModal" :users="users" />
      <EditUserModal v-if="editUser" v-model:visible="editUser" v-bind:user="selectedUser" />
      <AddUserModal v-if="addUser" v-model:visible="addUser" />
    </section>
  </main>
</template>

<style>
:root {
  --sidebar-width: 78px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

body {
  width: 100%;
  background: rgb(223, 222, 222);
}
</style>

<style scoped>
main {
  margin-left: var(--sidebar-width);
  padding: 0 3em 3em;
}

.content {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.title {
  color: #444a53;
  font-size: 30px;
  margin-left: 3rem;
  font-weight: 700;
}
</style>