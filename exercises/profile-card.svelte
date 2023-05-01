<script>
  let customer = "Maria Gonzales";
  let profilePic = "https://randomuser.me/api/portraits/women/25.jpg";
</script>

<div class="profile-card">
  <div class="container-card">
    <h1 class="profile-name">
      Welcome, <strong>{customer}</strong>
    </h1>
    <div class="wrapper-image">
      <img src={profilePic} alt="A randomly generate female profile" />
    </div>
  </div>
</div>

<style>
  .profile-card {
    width: 100%;
    height: 178px;
    background-color: orange;
  }

  .container-card {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 30px;
  }

  .profile-name {
    padding: 15px;
    font-size: 36px;
    color: white;
  }

  .profile-name strong {
    font-weight: 300;
  }

  .wrapper-image {
    display: flex;
    justify-self: center;
  }

  .wrapper-image img {
    border-radius: 50%;
    border: 1px solid #fff;
  }
</style>
