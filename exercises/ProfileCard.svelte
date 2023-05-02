<script>
  export let name, picture;

  let counter = 0;
  let message = "Clicked ";

  function trackClicks() {
    counter += 1;
  }

  function displayCount(message, counter) {
    if (counter === 1) {
      return `${message} ${counter} time`;
    } else if (counter > 1) {
      return `${message} ${counter} times`;
    }
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
    <button on:click={trackClicks} class="toggle-btn">
      {counter > 0 ? displayCount(message, counter) : "More Info"}
    </button>
  </div>
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
</style>
