<script lang="ts">

</script>

<div>
  <h2>Architects</h2>
  <div class="page-content-top">
    <div class="profile-card">
      <div class="profile-image">
        <i class="fa fa-user fa-5x" aria-hidden="true"></i>
      </div>

      <div class="profile-info">
        <p style="float: left;">&nbsp &nbsp John Doe</p>
        <p style="float: right">14 yrs xp &nbsp</p>
        <a href="/portfolio?name=john_doe">See Portfolio</a>
      </div>
    </div>

    <div class="profile-card">
      <div class="profile-image">
        <i class="fa fa-user fa-5x" aria-hidden="true"></i>
      </div>

      <div class="profile-info">
        <p style="float: left;">&nbsp &nbsp James Roe</p>
        <p style="float: right">8 yrs xp &nbsp</p>
        <a href="/portfolio?name=james_roe">See Portfolio</a>
      </div>

    </div>

    <div class="profile-card">
      <div class="profile-image">
        <i class="fa fa-user fa-5x" aria-hidden="true"></i>
      </div>

      <div class="profile-info">
        <p style="float: left;">&nbsp &nbsp Jane Poe</p>
        <p style="float: right">8 yrs xp &nbsp</p>
        <a href="/portfolio?name=jane_poe">See Portfolio</a>
      </div>

    </div>
  </div>

  <div class="page-content-bottom">
    <div class="profile-card">
      <div class="profile-image">
        <i class="fa fa-user fa-5x" aria-hidden="true"></i>
      </div>

      <div class="profile-info">
        <p style="float: left;">&nbsp &nbsp Anne Cox</p>
        <p style="float: right">5 yrs xp &nbsp</p><br/>
        <a href="/portfolio?name=anne_cox">See Portfolio</a>
      </div>

    </div>

    <div class="profile-card">
      <div class="profile-image">
        <i class="fa fa-user fa-5x" aria-hidden="true"></i>
      </div>

      <div class="profile-info">
        <p style="float: left;">&nbsp &nbsp Ben Fox</p>
        <p style="float: right">7 yrs xp &nbsp</p>
        <a href="/portfolio?name=ben_fox">See Portfolio</a>
      </div>
    </div>

    <div class="profile-card">
      <div class="profile-image">
        <i class="fa fa-user fa-5x" aria-hidden="true"></i>
      </div>

      <div class="profile-info">
        <p style="float: left;">&nbsp &nbsp Liz Day</p>
        <p style="float: right">3 yrs xp &nbsp</p>
        <a href="/portfolio?name=liz_day">See Portfolio</a>
      </div>
    </div>
  </div>

</div>

<style>
.page-content-top {
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
}

.page-content-bottom {
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
}

.profile-card {
    box-sizing: border-box;
    border: 1px solid white;
    border-radius: 20px;
    margin: 3em;
    width: 200px;
    height: 225px;
}

.profile-card:hover {
    transform: scale(1.15);
}

.profile-image {
    box-sizing: border-box;
    width: 200px;
    height: 125px;
    padding: 5px;
}

.profile-info {
    box-sizing: border-box;
    width: 200px;
    height: 100px;
}

.profile-info a {
    float: left;
    box-sizing: border-box;
    margin-left: 0.95em;
    margin-bottom: 0.5em;
    padding: 0.25em;
    color: white;
    text-decoration: underline;
    font-size: 0.85em;
}

.profile-info a:hover {
    color: darkgrey;
}

@media (prefers-color-scheme: light) {
  .profile-card {
    border: 1px solid black;
  }

  .profile-info a {
    color: black;
  }
  
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
    .page-content-top {
    display: flex;
    flex-direction: column;
}

    .page-content-bottom {
    display: flex;
    flex-direction: column;
    }
}

</style>


