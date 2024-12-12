<template>
    <div class="board">
      <table width="100%">
        <thead>
          <tr>
            <td>Name</td>
            <td>Phone Number</td>
            <td>Status</td>
            <td>Date Join</td>
            <td></td>
          </tr>
        </thead>
        <tbody>
            <tr>
  <td class="People">
    <img src="@/assets/image/1.image.jpg" alt="User Image">
    <div class="people-de">
      <h5>Kaguya Gintama</h5>
      <p>kaguya@gmail.com</p>
    </div>
  </td>
  <td class="people-phone"><p>011-2367859</p></td>
  <td class="active"><p>Active</p></td>
  <td class="datejoin"><p>11 November 2020</p></td>
  <td class="edit">
    <button class="edit-btn" @click="editUser('Kaguya Gintama', '@/assets/image/1.image.jpg', '2000-11-11', 'Female', '011-2367859', 'kaguya@gmail.com', 'Active')">
      <i class="bx bx-edit"></i>
      Edit
    </button>
  </td>
</tr>
<tr>
                        <td class="People">
                            <img src="@/assets/image/image.8.jpg" alt="">
                            <div class="people-de">
                                <h5>Jennie Whittaker</h5>
                                <p>JennieWhit123@gmail.com</p>
                            </div>
                        </td>


                        <td class="people-phone"><p>011-2322259</p></td>


                        <td class="active"><p>Active</p></td>


                        <td class="datejoin"><p>31 December 2020</p></td>


                        <td class="edit">
                            <button class="edit-btn" onclick="editUser('Kaguya Gintama', '@/assets/image/image.8.jpg', '2000-11-11', 'Female', '011-2367859', 'kaguya@gmail.com', 'Active')">
                                <i class="bx bx-edit"></i>
                                Edit
                            </button>
                        </td>
                       
                    </tr>
                    <tr>
                        <td class="People">
                            <img src="@/assets/image/image.3.avif" alt="">
                            <div class="people-de">
                                <h5>Lee Soo Young</h5>
                                <p>LSY1107@gmail.com</p>
                            </div>
                        </td>


                        <td class="people-phone"><p>011-2367890</p></td>


                        <td class="active"><p>Active</p></td>


                        <td class="datejoin"><p>12 November 2020</p></td>


                        <td class="edit">
                            <button class="edit-btn" onclick="editUser('Kaguya Gintama', '@/assets/image/image.3.avif', '2000-11-11', 'Female', '011-2367859', 'kaguya@gmail.com', 'Active')">
                                <i class="bx bx-edit"></i>
                                Edit
                            </button>
                        </td>


                       
                    </tr>
                    <tr>
                        <td class="People">
                            <img src="@/assets/image/image.4.jpg" alt="">
                            <div class="people-de">
                                <h5>Kendrick Lamar</h5>
                                <p>KendLamar2200@gmail.com</p>
                            </div>
                        </td>


                        <td class="people-phone"><p>012-2367859</p></td>


                        <td class="active"><p>Active</p></td>


                        <td class="datejoin"><p>15 November 2020</p></td>


                        <td class="edit">
                            <button class="edit-btn" onclick="editUser('Kaguya Gintama', '@/assets/image/image.4.jpg', '2000-11-11', 'Female', '011-2367859', 'kaguya@gmail.com', 'Active')">
                                <i class="bx bx-edit"></i>
                                Edit
                            </button>
                        </td>


                       
                    </tr>
                    <tr>
                        <td class="People">
                            <img src="@/assets/image/image.5.jpg" alt="">
                            <div class="people-de">
                                <h5>John Mactavish Soap</h5>
                                <p>JMp141TFT@gmail.com</p>
                            </div>
                        </td>


                        <td class="people-phone"><p>011-2277859</p></td>


                        <td class="active"><p>Active</p></td>


                        <td class="datejoin"><p>23 November 2020</p></td>


                        <td class="edit">
                            <button class="edit-btn" onclick="editUser('Kaguya Gintama', '@/assets/image/image.5.jpg', '2000-11-11', 'Female', '011-2367859', 'kaguya@gmail.com', 'Active')">
                                <i class="bx bx-edit"></i>
                                Edit
                            </button>
                        </td>


                       
                    </tr>
                    <tr>
                        <td class="People">
                            <img src="@/assets/image/image.6.jpg" alt="">
                            <div class="people-de">
                                <h5>Brittney Spears</h5>
                                <p>BSohbaby1123@gmail.com</p>
                            </div>
                        </td>


                        <td class="people-phone"><p>011-2361111</p></td>


                        <td class="active"><p>Active</p></td>


                        <td class="datejoin"><p>11 December 2020</p></td>


                        <td class="edit">
                            <button class="edit-btn" onclick="editUser('Kaguya Gintama', '@/assets/image/image.6.jpg', '2000-11-11', 'Female', '011-2367859', 'kaguya@gmail.com', 'Active')">
                                <i class="bx bx-edit"></i>
                                Edit
                            </button>
                        </td>


                       
                    </tr>
                    <tr>
                        <td class="People">
                            <img src="@/assets/image/image.7.jpg" alt="">
                            <div class="people-de">
                                <h5>Mark Oboyi</h5>
                                <p>Markplier1100@gmail.com</p>
                            </div>
                        </td>


                        <td class="people-phone"><p>011-1111859</p></td>


                        <td class="active"><p>Active</p></td>


                        <td class="datejoin"><p>29 December 2020</p></td>


                        <td class="edit">
                            <button class="edit-btn" onclick="editUser('Kaguya Gintama', '@/assets/image/image.7.jpg', '2000-11-11', 'Female', '011-2367859', 'kaguya@gmail.com', 'Active')">
                                <i class="bx bx-edit"></i>
                                Edit
                            </button>
                        </td>


                       
                    </tr>


        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
  methods: {
    // Method to emit the event for opening the edit user modal
    editUser(name, image, dob, gender, phone, email, status) {
      // Create an object for the user data
      const user = {
        name,
        image,
        dob,
        gender,
        phone,
        email,
        status
      };

      // Emit an event to open the edit modal and pass the user data
      this.$emit('openEditUserPopup', user);
    },
  },
};
  </script>
  <style>
.board {
    width: 120%;
    margin: 30px 0 30px 30px;
    overflow: auto;
    background: white;
    border-radius: 8px;
    text-align: center;
}

.board img{
    width: 45px;
    height: 45px;
    object-fit: cover;
    border-radius: 50%;
    margin-right: 15px;
}

.board h5{
    font-weight: 600;
    font-size: 14px;
}

.board p{
    font-weight: 400;
    font-size: 13px;
    color: #787d8d;
}

.board .People{
    display: flex;
    justify-content: flex-start;
    align-items: center;
    text-align: start;
}

table{
    border-collapse: collapse;
}

tr{
    border-bottom: 1px solid #eef0f3;
}

thead td{
    font-size: 13px;
    font-family:"Pirata One", system-ui;
    color:rgb(94, 92, 92);
    text-transform: uppercase;
    font-weight: 500;
    background:#F9FAFB;
    padding: 15px;
}

thead td .bx-edit{
    text-decoration: none;
    font-size: 14px;
    color: rgb(22, 22, 99);
    font-weight: 600;
}

thead td .bx-edit:hover {
    background: #a73636;
    color: #11101D;

}
tbody tr td{
    padding: 10px 15px;
}
.active p{
background: #d7fada;
padding: 2px 10px;
display: inline-block;
border-radius: 40px;
color: #2b2b2b;
}

.edit a{
    text-decoration: none;
    font-size: 14px;
    color: rgb(22, 22, 99);
    font-weight: 600;
}

.edit-btn {
    background: none; /* Remove button background */
    border: none; /* Remove button border */
    color: inherit; /* Inherit text color */
    font: inherit; /* Inherit font properties */
    cursor: pointer; /* Show pointer cursor */
    display: flex; /* Allow for flex layout */
    align-items: center; /* Align icon and text */
    gap: 5px; /* Space between icon and text */
    padding: 5px 10px; /* Add padding for clickable area */
}

.edit-btn:hover {
    background-color: #f0f0f0; /* Optional: Hover effect */
    border-radius: 5px; /* Optional: Rounded corners */
}

.edit-btn:active {
    transform: scale(0.98); /* Optional: Click effect */
}
</style>