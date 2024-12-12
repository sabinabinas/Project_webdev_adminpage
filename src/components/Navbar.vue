<template>
  <div class="interface">
    <div class="navigation">
      <div class="n1">
        <div class="search">
          <i class="bx bx-search-alt"></i>
          <input type="text" placeholder="Search" />
        </div>
      </div>
      <div class="profile">
        <i class="bx bx-bell"></i>
        <img src="@/assets/image/1.image.jpg" />
      </div>
    </div>
  </div>
</template>

<style scoped>

.navigation {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #fdfdfd;
  padding: 20px 40px;
  border-bottom: 3px solid #594ef7;
  border-radius: 10px;
}

.navigation .search {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  border: 1px solid #d6dae3;
  padding: 5px 10px;
  border-radius: 10px;
}

.navigation .search i {
  margin-right: 14px;
  padding: 5px 10px;
}

.navigation .search input {
  border: none;
  outline: none;
  font-size: 14px;
}

.navigation .profile {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.navigation .profile i {
  margin-right: 20px;
  font-size: 19px;
  font-weight: 400;
}

.navigation .profile img {
  width: 40px;
  height: 40px;
  object-fit: cover;
  border-radius: 50%;
}

.n1 {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.interface .i-name {
  color: #444a53;
  /* padding: 15px 15px 0 15px; */
  font-size: 30px;
  font-weight: 700;
  /* margin-top: 20px; */
}
</style>