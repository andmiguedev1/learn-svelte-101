<script>
  let customer = "Maria Gonzales";
  let profilePic = "https://randomuser.me/api/portraits/women/25.jpg";
</script>

<section class="profile-area">
  <div class="profile-card">
    <div class="content">
      <div class="profile-image">
        <img src={profilePic} alt={customer} />
      </div>
      <div class="profile-info">
        <h2>{customer}</h2>
        <br />
        <span>Digital Marketing</span>
      </div>
      <span class="toggle-btn" />
    </div>
  </div>
</section>

<style>
  @import url("https://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900");

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Poppins", Arial, sans-serif;
  }

  .profile-area {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f1f1f1;
  }
  .profile-card {
    height: 100px;
    transition: 0.5s;
  }
  .profile-card .content {
    position: relative;
    width: 400px;
    min-height: 150px;
    padding: 60px 40px 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 10px;
    background-color: orange;
    border-radius: 10px;
  }
  .profile-card .profile-image {
    position: absolute;
    top: 0;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    border: 6px solid #fff;
    transform: translateY(-50%);
    transition: all 0.5s ease;
    overflow: hidden;
    z-index: 9;
  }
  .profile-card .profile-image img {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .profile-card .profile-info {
    position: relative;
    text-align: center;
  }
  .profile-card .profile-info h2 {
    font-size: 1.25em;
    font-weight: 500;
    line-height: 1.05em;
    color: #fff;
  }
  .profile-card .profile-info span {
    font-size: 0.89em;
    font-weight: 300;
    color: #f1f1f1;
  }
  .profile-card .toggle-btn {
    position: absolute;
    bottom: 0;
    width: 120px;
    padding: 5px 15px;
    font-size: 0.8em;
    text-align: center;
    background-color: #fff;
    color: orange;
    border: 6px solid #f2eded;
    border-radius: 30px;
    transform: translateY(50%);
    transition: all 0.5s ease-out;
    cursor: pointer;
  }
  .profile-card .toggle-btn::before {
    content: "More Info";
  }
</style>
