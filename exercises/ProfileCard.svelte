<script>
  export let name, picture;

  let profile = {
    onClick: false,
  };

  function toggleBtn() {
    profile.onClick = !profile.onClick;
  }
</script>

<article class="profile-card">
  <div class="content">
    <div class="profile-image">
      <img src={picture} alt={name} />
    </div>
    <div class="profile-info">
      <h2>{name}</h2>
      <span>Digital Marketing</span>
    </div>
    {#if profile.onClick}
      <button on:click={toggleBtn} class="toggle-btn"> More Info </button>
    {/if}
    {#if !profile.onClick}
      <button on:click={toggleBtn} class="toggle-btn"> Close </button>
    {/if}
  </div>
  {#if !profile.onClick}
    <div class="profile-details">
      <div class="profile-data">
        <div class="icon-box">
          <i class="bi bi-calendar" />
          <p>May, 2, 2023</p>
          <h5>Joined On</h5>
        </div>
      </div>
      <div class="profile-data">
        <div class="icon-box">
          <i class="bi bi-calendar" />
          <p>May, 2, 2023</p>
          <h5>Last login</h5>
        </div>
      </div>
    </div>
  {/if}
</article>

<style>
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
    min-width: 120px;
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
  .profile-card .toggle-btn:hover {
    color: #000;
  }
  .profile-details {
    display: flex;
    flex-direction: row;
    flex-flow: nowrap;
    background-color: #fff;
    padding: 0 15px;
    max-width: 500px;
  }
  .profile-details .profile-data {
    align-items: center;
    justify-content: space-between;
    flex-basis: 50%;
    margin: 0 10%;
  }
  .profile-details .profile-data p {
    font-size: 0.95em;
    font-weight: 500;
  }
  .profile-details .profile-data h5 {
    font-size: 0.65em;
    font-weight: 700;
    color: orange;
  }
</style>
