<template>
  <div class="container1">
    <div>
      <h1>My Profil</h1>
      <ul class="data">
        <li class="profile-name">Profile Name</li>
        <li class="email"> <img class="email-img" src="img/email.png" />Email</li>
        <li class="phone"> <img class="phone-img" src="img/phone.png" />Phone</li>
        <li class="location">LOCATION</li>
        <li class="country">Country:</li>
        <li class="city">City:</li>
        <li class="education">EDUCATION</li>
        <li class="year1">2003</li>
        <li class="high-school">High School</li>
        <li class="year2">2003</li>
        <li class="degree">Degree</li>
      </ul>
      <button class="edit-btn"> <img class="pen-img" src="img/pen.png" />EDIT</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container1{
  display: grid;
  position: absolute;
  top: 140px;
  left: 260px;
  display:none;
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
.profile-name{
  font-weight: bold;
  font-size: 25px;
  line-height: 30px;
  letter-spacing: 1px;
}
.email, .phone {
  font-size: 16px;
  line-height: 23px;
  margin-top: 16px;
}
.email-img, .phone-img{
  margin-right: 15px;
  position: relative;
  top: 2px;
}
.location, .education{
  font-weight: bold;
  font-size: 16px;
  line-height: 30px;
  margin-top: 30px;
  margin-bottom: 15px;
}
.country, .city{
  font-size: 16px;
  line-height: 23px;
  margin: 0px 0px 10px 0px;
}
.year1, .year2{
  font-weight: bold;
  font-size: 16px;
  line-height: 23px;
  margin-bottom: 10px;
}
.high-school, .degree{
  font-size: 16px;
  line-height: 23px;
  margin-bottom: 10px;
}
.edit-btn{
  width: 155px;
  height: 59px;
  left: 261px;
  top: 707px;
  background: #FFFFFF;
  box-shadow: 0px 5px 10px rgba(56, 59, 55, 0.2);
  border-radius: 30px;
  border: 1px solid white;
  margin-top: 30px;
  font-weight: bold;
  font-size: 16px;
  line-height: 23px;
  cursor: pointer;
}
.pen-img{
  height: 18px;
  position: relative;
  top: 3px;
  right: 20px;
}
</style>