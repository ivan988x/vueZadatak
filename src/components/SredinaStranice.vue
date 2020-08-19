<template>
  <div>
    <!-- Prva stranica -->
    <div class="container">
      <h1>My Profil</h1>
      <div class="miniContainer">
        <h2>Edit Account information</h2>
      </div>

      <div class="container2">
        <div class="left">
          <h3>PERSONAL</h3>
          <label for>First Name</label>
          <input required type="text" placeholder="John" v-model="firstName" />
          <label for>Last Name</label>
          <input required type="text" placeholder="Johnes" v-model="lastName" />
          <label for>Email Address</label>
          <input required type="text" placeholder="john.johnes@gmail.com" v-model="email" />
          <label for>Phone</label>
          <input required type="text" placeholder="+385 91 111 111" v-model="phone" />

          <h3>LOCATION</h3>
          <label for>Country</label>
          <input required type="text" placeholder="Enter Country" v-model="country" />
          <label for>City</label>
          <input required type="text" placeholder="Enter City" v-model="city" />
        </div>

        <div class="right">
          <h3>EDUCATION</h3>
          <label class="education" for>Education</label>
          <label class="finished" for>Finished</label>
          <input type="text" placeholder="Enter Country" v-model="education1" />
          <select name="year" id="year" v-model="education1_year">
            <option value="2003">2003</option>
          </select>

          <input type="text" placeholder="Enter City" v-model="education2" />
          <select name="year" id="year" v-model="education2_year">
            <option value="2003">2008</option>
          </select>

          <div class="add">
            <img class="add-icon" src="img/icon.png" />
            <a class="add-link">Add</a>
          </div>

          <button class="save" v-on:click="save()">SAVE CHANGES</button>
        </div>
      </div>
    </div>

    <!-- Druga stranica -->
    <div class="container1">
      <div class="data" v-for="data in params" :key="data.id">
        <h1>My Profil</h1>
        <ul class="data">
          <li class="profile-name">Profile {{get_data.first_name}}</li>
          <li class="email">
            <img class="email-img" src="img/email.png" />Email {{get_data.email}}
          </li>
          <li class="phone">
            <img class="phone-img" src="img/phone.png" />Phone {{get_data.phone}}
          </li>
          <li class="location">LOCATION</li>
          <li class="country">Country: {{get_data.country}}</li>
          <li class="city">City: {{get_data.city}}</li>
          <li class="education">EDUCATION</li>
          <li class="year1">2003 {{get_data.education1_year}}</li>
          <li class="high-school">High School {{get_data.education1}}</li>
          <li class="year2">2003 {{get_data.education2_year}}</li>
          <li class="degree">Degree {{get_data.education2}}</li>
        </ul>
        <button class="edit-btn">
          <img class="pen-img" src="img/pen.png" />EDIT
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    save: function () {
      alert("message");
      const axios = require("axios");
      axios
        .get("https://factory.hr/api/test.php", {
          params: {
            // Trebam još pokupiti vrijednosti iz inputa, kreirati objekt i ovdje ga poslati
            first_name: this.firstName,
            last_name: this.lastName,
            email: this.email,
            phone: this.phone,
            country: this.country,
            city: this.city,
            education1: this.education1,
            education1_year: this.education1_year,
            education2: this.education2,
            education2_year: this.education2_year,
          },
        })
        .then(function(res){
          this.params = res.data.get_data;
          console.log('Data: ',res.data.get_data);
        })
          // Ovdje se dohvaćaju vraćeni podaci
       
        .catch(function (error) {
          console.log(error);
        });
    },
  },
  data: function () {
    return {
      firstName: "",
      lastName: "",
      email: "",
      phone: "",
      country: "",
      city: "",
      education1: "",
      education1_year: "",
      education2: "",
      education2_year: "",
    };
  },
};
</script>

<style scoped>
/* ------------------------------------------------------------------------------ Antonio */

.container2 {
  display: flex;
  justify-content: center;

  width: 924px;
  margin: 0 auto;
}

.miniContainer {
  width: 924px;
  margin: 0 auto;
}

h1 {
  font-weight: bold;
  font-size: 45px;
  line-height: 25px;
  margin-top: 60px;
  margin-bottom: 30px;
}

h2 {
  font-size: 25px;
  line-height: 30px;
  letter-spacing: 1px;
  color: #1d1d1d;
}

h3 {
  font-size: 16px;
  line-height: 30px;
  letter-spacing: 1px;
  color: #1d1d1d;

  margin-bottom: 5px;
  margin-top: 30px;
}

label {
  font-size: 16px;
  line-height: 23px;
  color: #383b37;

  display: block;
  margin-left: 20px;
  margin-bottom: 5px;
}

input {
  border: 1px solid #cccccc;
  box-sizing: border-box;
  box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.08);

  width: 440px;
  height: 50px;

  font-size: 16px;
  padding-left: 20px;
  margin-bottom: 15px;
}
input:hover {
  box-shadow: 0px 5px 20px #c4c4c4;
}

.left {
  margin-right: 40px;
}

.right label {
  display: inline-block;
}
.finished {
  margin-left: 249px;
}
.right input {
  width: 316px;
  margin-bottom: 10px;
  margin-right: 5px;
}

select {
  width: 119px;
  height: 50px;

  border: 1px solid #cccccc;
  box-sizing: border-box;
  box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.08);

  font-size: 16px;
  display: inline-block;
  padding-left: 20px;
}
select:hover {
  box-shadow: 0px 5px 20px #c4c4c4;
}

.add {
  display: flex;
  justify-content: flex-start;

  padding: 12px;
  height: 44px;

  margin-bottom: 30px;
}

.add-link {
  font-weight: normal;
  font-size: 16px;
  line-height: 23px;
  color: #85b2ff;
  margin-left: 12px;
}
.add-link:hover {
  cursor: pointer;
}

.save {
  float: right;

  background: #575756;
  border-radius: 30px;
  width: 221px;
  height: 59px;

  font-size: 16px;
  line-height: 23px;
  text-align: center;
  letter-spacing: 2px;
  color: #ffffff;
  border: none;
  outline: none;
  box-shadow: 0px 5px 10px rgba(56, 59, 55, 0.2);
}

.save:hover {
  cursor: pointer;
}

/* ------------------------------------------------------------------------------ Ivan */

.container1 {
  display: grid;
  position: absolute;
  top: 140px;
  left: 260px;
  
}
h1 {
  font-family: Arial;
  font-style: normal;
  font-weight: bold;
  font-size: 45px;
  line-height: 25px;
}
.data {
  margin-top: 70px;
}
.profile-name {
  font-weight: bold;
  font-size: 25px;
  line-height: 30px;
  letter-spacing: 1px;
}
.email,
.phone {
  font-size: 16px;
  line-height: 23px;
  margin-top: 16px;
}
.email-img,
.phone-img {
  margin-right: 15px;
  position: relative;
  top: 2px;
}
.location,
.education {
  font-weight: bold;
  font-size: 16px;
  line-height: 30px;
  margin-top: 30px;
  margin-bottom: 15px;
}
.country,
.city {
  font-size: 16px;
  line-height: 23px;
  margin: 0px 0px 10px 0px;
}
.year1,
.year2 {
  font-weight: bold;
  font-size: 16px;
  line-height: 23px;
  margin-bottom: 10px;
}
.high-school,
.degree {
  font-size: 16px;
  line-height: 23px;
  margin-bottom: 10px;
}
.edit-btn {
  width: 155px;
  height: 59px;
  left: 261px;
  top: 707px;
  background: #ffffff;
  box-shadow: 0px 5px 10px rgba(56, 59, 55, 0.2);
  border-radius: 30px;
  border: 1px solid white;
  margin-top: 30px;
  font-weight: bold;
  font-size: 16px;
  line-height: 23px;
  cursor: pointer;
}
.pen-img {
  height: 18px;
  position: relative;
  top: 3px;
  right: 20px;
}
</style>
