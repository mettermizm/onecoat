<template>
  <div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-6">
          <h1 class="large-text">NATURA</h1>
        </div>
        <div class="col-md-1"></div>
        <div class="col-md-4">
          <Logo />
          <Search />
        </div>
        <div class="col-md-11">
          <p>
            Natura Onecoat is an all-in-one, eco-friendly wood oil stain that
            simplifies wood finishing for woodworkers. This innovative product
            combines the protective qualities of a hard wax oil with the
            aesthetic benefits of a stain, all achievable in a single
            application. Crafted from 100% natural ingredients, it
          </p>
        </div>
        <div class="col-md-6"></div>
        <div class="col-md-6">
          <Before />
        </div>

        <div class="urun_wrap">
          <div class="center1">
            <div class="urun_grid">
              <div class="content">
                <div class="title">ALL IN</div>
                <div class="subtitle">ONE COAT</div>
                <div class="icerik">
                  <strong>Once upon a time,</strong> in a quaint little town,
                  nestled between rolling hills and serene meadows, there stood
                  a coffee company named Osso. It was no ordinary company; it
                  was a sanctuary for coffee lovers, a place where the art of
                  brewing was taken to new heights. The journey of Osso began
                  with a passionate group of coffee enthusiasts. They roamed the
                  world, from the misty plantations of Colombia to the bustling
                  markets of Ethiopia, in search of the finest coffee beans.
                  Each bean was carefully selected, a testament to Osso’s
                  commitment to quality.
                </div>
              </div>
              <div class="gorsel">
                <img src="~/assets/img/naturaproduct.png" alt="" srcset="" />
              </div>
            </div>
          </div>
        </div>

        <div class="skils_wrap">
          <div class="center2">
            <div class="skils_grid">
              <div class="item">
                <div class="ikon">
                  <img src="~/assets/img/skils/paintbrush.png" />
                </div>
                <div class="info">SINGLE COAT</div>
              </div>
              <div class="item">
                <div class="ikon">
                  <img src="~/assets/img/skils/vegan.png" />
                </div>
                <div class="info">VOC FREE</div>
              </div>
              <div class="item">
                <div class="ikon">
                  <img src="~/assets/img/skils/Union 1.png" />
                </div>
                <div class="info">EN 71-3</div>
                <div class="info_sub">SAFETY FOR TOYS</div>
              </div>
              <div class="item">
                <div class="ikon">
                  <img src="~/assets/img/skils/addition-thick-symbol.png" />
                </div>
                <div class="info">MORE AREA</div>
              </div>
            </div>
          </div>
        </div>

        <div class="slogan_wrap">
          <div class="center3">
            <div class="slogan_text">“Pure Touch in Everyway.”</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.center1 {
  width: 1600px;
  max-width: 96%;
  margin: 0 auto;
}

.center2 {
  width: 1400px;
  max-width: 96%;
  margin: 0 auto;
}

.center3 {
  width: 1200px;
  max-width: 96%;
  margin: 0 auto;
}

.urun_wrap .urun_grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  margin: 20px 0px;
  gap: 20px;
}
.urun_wrap .urun_grid .content {
  align-items: left;
  text-align: left;
}
.urun_wrap .urun_grid .content .title {
  text-align: left;
  font: normal normal normal 88px/120px Avenir;
  letter-spacing: 0px;
  color: #0e112c;
  opacity: 1;
}
.urun_wrap .urun_grid .content .subtitle {
  text-align: left;
  font: normal normal 900 88px/120px Avenir;
  letter-spacing: 0px;
  color: #0e112c;
  opacity: 1;
}
.urun_wrap .urun_grid .content .icerik {
  text-align: left;
  letter-spacing: 0px;
  color: #000000;
  opacity: 1;
}

.urun_wrap .urun_grid .gorsel {
  text-align: center;
}
.skils_wrap {
  margin: 20px 0px;
}

.skils_wrap .skils_grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 30px;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.skils_wrap .skils_grid .item {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2px;
}

.slogan_wrap .slogan_text {
  margin: 0 0 60px 0;
  text-align: center;
  font-family: 'avenir_roman';
  letter-spacing: 22px;
  font-size: 2rem;
}
</style>
