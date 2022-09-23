<template>
  <input type="checkbox" id="check">
  <label for="check">
    <ion-icon name="menu" id="btn"></ion-icon>
    <ion-icon name="close" id="cancel"></ion-icon>
  </label>
  <div class="sidebar">
    <header class="sidebar__title">
      MyApp
    </header>
    <ul class="sidebar__list">
      <li class="sidebar__item"><a class="sidebar__link" href="#"><ion-icon name="layers-outline"></ion-icon>Lessons</a></li>
      <li class="sidebar__item"><a class="sidebar__link" href="#"><ion-icon name="library-outline"></ion-icon>Books</a></li>
      <li class="sidebar__item"><a class="sidebar__link" href="#"><ion-icon name="mail-outline"></ion-icon>Messages</a></li>
      <li class="sidebar__item"><a class="sidebar__link" href="#"><ion-icon name="megaphone-outline"></ion-icon>Anouncements</a></li>
      <li class="sidebar__item"><a class="sidebar__link" href="#"><ion-icon name="play-circle-outline"></ion-icon>Media</a></li>
      <li class="sidebar__item"><a class="sidebar__link" href="#"><ion-icon name="settings-outline"></ion-icon>Settings</a></li>
      <li class="sidebar__item"><a class="sidebar__link" href="#"><ion-icon name="help-circle-outline"></ion-icon>Help</a></li>
    </ul>
  </div>
  <section class="hero">
    <h1>Content Here</h1>
  </section>
</template>

<script>
export default {
  name: 'Navbar',
  props: {
    msg: String
  }
}
</script>


<style scoped>
  .sidebar {
    position: fixed;
    left: -250px;
    width: 250px;
    height: 100%;
    background: #042331;

    transition: all .4s ease;
  }
  .sidebar__title {
      font-size: 20px;
      color: #fff;
      user-select: none;
      line-height: 70px;
      text-align: center;
      background: #063146;
    }


  .sidebar__link {
    display: flex;
    align-items: center;
    gap: 5px;
    height: 100%;
    width: 100%;
    line-height: 65px;
    font-size: 20px;
    color: #fff;
    box-sizing: border-box;
    padding-left: 40px;
    border-top: 1px solid rgba(255, 255, 255, .1);
    border-bottom: 1px solid rgba(0, 0, 0, .9);

    transition: all .4s ease;
  }

  .sidebar__list .sidebar__item:hover .sidebar__link {
    padding-left: 50px;
    gap: 10px;
    color: #9ABFE8;
  } 

  #check {
    display: none;
  }

  label #btn, label #cancel {
    position: absolute;
    cursor: pointer;
    background: #042331;
    border-radius: 5px;
  }
  label #btn {
    left: 40px;
    top: 25px;
    font-size: 35px;
    color: #fff;
    padding: 6px 12px;

    transition: all .3s ease;
  }

  label #cancel {
    left: -185px;
    top: 19px;
    font-size: 25px;
    color: #0a5275;
    padding: 4px 8px;

    z-index: 99;
    transition: all .4s ease;
  }

  #check:checked ~ .sidebar {
    left: 0;
  }
  
  #check:checked ~ label #btn {
    opacity: 0;
    left: 260px;
    pointer-events: none;
  }
  #check:checked ~ label #cancel {
    left: 185px;
  }

  .hero {
    background: url(../assets/hero.jpg) no-repeat;
    background-size: cover;
    background-position: center;
    height: 100vh;
    color: aqua;

    display: flex;
    justify-content: center;
    align-items: center;

    transition: all .4s ease;
  }

  #check:checked ~ .hero {
    margin-left: 250px;
  }
</style>
