<template>
  <div class="container">
    <h1>My Profil</h1>
    <div class="container">
      <h2>Edit Account information</h2>
      <div>
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

      <div>
        <h3>EDUCATION</h3>
        <label for>Education</label>
        <label for>Finished</label>
        <input type="text" placeholder="Enter Country" />
        <select name="year" id="year">
          <option value="2003">2003</option>
        </select>

        <input type="text" placeholder="Enter City" />
        <select name="year" id="year">
          <option value="2003">2008</option>
        </select>

        <button>Add</button>
        <button>SAVE CHANGES</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>