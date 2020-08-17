<template>
  <div class="container">
    <h1>My Profil</h1>
    <div class="miniContainer">
      <h2>Edit Account information</h2>
    </div>

    <div class="container2">
      <div class="left">
        <h3>PERSONAL</h3>
        <label for>First Name</label>
        <input type="text" placeholder="John" />
        <label for>Last Name</label>
        <input type="text" placeholder="Johnes" />
        <label for>Email Address</label>
        <input type="text" placeholder="john.johnes@gmail.com" />
        <label for>Phone</label>
        <input type="text" placeholder="+385 91 111 111" />

        <h3>LOCATION</h3>
        <label for>Country</label>
        <input type="text" placeholder="Enter Country" />
        <label for>City</label>
        <input type="text" placeholder="Enter City" />
      </div>

      <div class="right">
        <h3>EDUCATION</h3>
        <label class="education" for>Education</label>
        <label class="finished" for>Finished</label>
        <input type="text" placeholder="Enter Country" />
        <select name="year" id="year">
          <option value="2003">2003</option>
        </select>

        <input type="text" placeholder="Enter City" />
        <select name="year" id="year">
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
</template>

<script>
export default {
  methods: {
    save: function() {
      alert("message");
      const axios = require("axios");
      axios
        .get("https://factory.hr/api/test.php", {
          params: {
            // Trebam još pokupiti vrijednosti iz inputa, kreirati objekt i ovdje ga poslati
            ID: 12345,
          },
        })
        .then(function(response) {
          console.log(response);
          // Ovdje se dohvaćaju vraćeni podaci
        })
        .catch(function(error) {
          console.log(error);
        });
    },
  },
};
</script>

<style scoped>
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
</style>
