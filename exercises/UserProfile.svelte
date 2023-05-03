<script>
  import ProfileCard from "./ProfileCard.svelte";

  const customer = {
    name: "Jessica Gonzales",
    age: 26,
    profilePic: "https://randomuser.me/api/portraits/women/25.jpg",
    job: "Digital Marketing",
    favoriteFood: "Chicken Picatta",
  };
</script>

<section class="user-profile">
  <ProfileCard name={customer.name} picture={customer.profilePic} />
</section>

<style>
  @import url("https://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900");

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Poppins", Arial, sans-serif;
  }

  .user-profile {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f1f1f1;
  }
</style>
