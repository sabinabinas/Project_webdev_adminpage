<template>
    <div class="interface">
    <div class="values">
      <div class="val-box">
        <i class="bx bx-user"></i>
        <div>
          <h3>2,000</h3>
          <span>Total Users</span>
        </div>
      </div>
      <div class="val-box">
        <i class="bx bx-user-check"></i>
        <div>
          <h3>1,588</h3>
          <span>Active Users</span>
        </div>
      </div>
      <div class="val-box">
        <i class="bx bx-user"></i>
        <div>
          <h3>200</h3>
          <span>New Users</span>
        </div>
      </div>
      <!-- Add New User Button -->
      <button class="val-box" @click="$emit('openAddUserPopup')">
        <i class="bx bx-user-plus"></i>
        <div>
          <h3>Add New User</h3>
        </div>
      </button>
    </div>
</div>
  </template>
  
  <script>
  export default {
    methods: {
      // No direct modal logic here as the modal is likely in a parent component
      emitAddUserPopup() {
        this.$emit('openAddUserPopup');
      },
    },
  };
  </script>

  <style>
#interface{
    width: 100%;
    margin-left:100px;
    position: relative;
}
.values{
    padding: 30px 30px 0 30px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    width: 120%;

}

.values .val-box{
    background: white;
    width: 235px;
    padding: 16px 20px;
    border-radius: 5px;
    display: flex;
    justify-content: flex-start;
    align-items: center ;
}


.values .val-box i{
    font-size: 25px;
    width: 60px;
    height: 60px;
    line-height: 60px;
    border-radius: 50%;
    text-align: center;
    color: white;
    margin-right: 15px;
}

.values .val-box:nth-child(1) i{
    background: palevioletred;
}

.values .val-box:nth-child(2) i{
    background: powderblue;
}

.values .val-box:nth-child(3) i{
    background: greenyellow;
}

.values .val-box:nth-child(4) i{
    background: rgb(227, 47, 255);
}

.values .val-box h3{
    font-size: 18px;
    font-weight: 600;
}

.values .val-box span{
    font-size: 15px;
    color: #828997;
}

button.val-box {
  background: none; /* Remove button background */
  border: none; /* Remove button border */
  cursor: pointer; /* Add pointer cursor */
  display: flex; /* Allow for flex layout */
  align-items: center; /* Align items in the center */
  justify-content: center; /* Center content */
  padding: 10px;
  margin: 5px;
}

button.val-box:hover {
    background-color: #f1f1f1; /* Optional: Add hover effect */
}

button.val-box:active {
    transform: scale(0.98); /* Optional: Add click effect */
}</style>