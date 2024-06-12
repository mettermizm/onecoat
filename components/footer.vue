<template>
  <footer id="footer1">
    <a href="#" class="up-button"><i class="fa-solid fa-chevron-up"></i></a>

    <div class="sect10" v-html="footerText1"></div>

    <div class="sect20">
      <div class="standard_center1">
        <div class="grid">
          <div class="s s1">
            <div class="iconlu1">
              <table>
                <tr>
                  <td><i class="fa-solid fa-globe"></i></td>
                  <td>{{ footerLeft1Title }}</td>
                </tr>
              </table>
            </div>
          </div>
          <div class="s s2">
            <div class="iconlu1">
              <table>
                <tr>
                  <td><i class="fa-regular fa-envelope"></i></td>
                  <td>{{ footerRight1Title }}</td>
                </tr>
              </table>
            </div>
          </div>
          <div class="s s3">{{ footerLeft1Text1 }}</div>
          <div class="s s4">{{ footerRight1Text1 }}</div>
          <div class="s s5">
            <a href="#">{{ footerLeft1Text2 }}</a>
          </div>
          <div class="s s6">
            <a :href="`mailto:${footerRight1Mail}`">{{ footerRight1Mail }}</a>
          </div>
        </div>
      </div>
    </div>

    <div class="sect30">
      <div class="standard_center1">
        <div class="grid">
          <div class="s s1"><div class="bos"></div></div>
          <div class="s s2">
            <form
              id="form_mail_abonelik"
              action="/back"
              method="POST"
              @submit.prevent="submitForm"
            >
              <input type="hidden" name="router" value="mail_abonelik" />
              <div class="grid2">
                <div class="grid2s s1">
                  <input type="email" v-model="email" placeholder="email" />
                </div>
                <div class="grid2s s2">
                  <button>{{ footerSubscribeFormButton }}</button>
                  <img
                    class="loading"
                    src="/static/img/loading/bar24.svg"
                    alt=""
                  />
                </div>
              </div>
            </form>
            <div class="text1">{{ footerSocialExplain }}</div>
          </div>
        </div>
      </div>
    </div>

    <div class="sect40">
      <div class="standard_center1">
        <div class="grid">
          <div class="s s1">
            <a :href="websiteLang">
              <img :src="headerLogo" alt="" />
            </a>
          </div>
          <div class="s s2">
            <div class="grid2" v-for="nav in footerNavs" :key="nav.title">
              <div class="grid2s">
                <div class="navtitle">{{ nav.title }}</div>
                <div class="list" v-html="nav.html"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="standard_center1">
      <div class="sect50">
        <div class="text1">{{ footerSocialExplain }}</div>
        <div class="icons">
          <a
            href="https://www.instagram.com/kollektmagofficial/"
            target="_blank"
            ><i class="fa-brands fa-instagram"></i
          ></a>
          <a
            href="https://www.youtube.com/channel/UCRrxYuHiH-6KvvoYuN_VKxA"
            target="_blank"
            ><i class="fa-brands fa-youtube"></i
          ></a>
          <a href="mailto:info@kollektmag.com" target="_blank"
            ><i class="fa-regular fa-envelope"></i
          ></a>
          <a
            href="https://www.linkedin.com/company/kollekt-mag-official/"
            target="_blank"
            ><i class="fa-brands fa-linkedin-in"></i
          ></a>
          <a
            href="https://twitter.com/i/flow/login?redirect_after_login=%2FKollektMag"
            target="_blank"
            ><i class="fa-brands fa-twitter"></i
          ></a>
          <a href="https://www.facebook.com/kollektmedya" target="_blank"
            ><i class="fa-brands fa-facebook"></i
          ></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      footerText1: 'is a <b>Journey</b>.',
      footerLeft1Title: 'Location',
      footerRight1Title: 'Contact',
      footerLeft1Text1: 'We have one and only location in İzmir.',
      footerRight1Text1: 'If you think you need, we are ready for the help.',
      footerLeft1Text2: 'Bostanlı, İzmir / TURKEY',
      footerRight1Mail: 'info@kollektmag.com',
      email: '',
      footerSubscribeFormButton: 'Contact Us',
      footerSocialExplain:
        'We will never share your email address & you can opt out at any time, we promise.',
      websiteLang: '/en',
      headerLogo: '/path/to/logo.png',
      footerNavs: [
        { title: 'Contact Us', html: "<div><a href='#'>We are?</a></div>" },
        { title: 'About Us', html: "<div><a href='#'>Who we are?</a></div>" },
        { title: 'Services', html: "<div><a href='#'>What we do?</a></div>" },
      ],
    }
  },
  methods: {
    submitForm() {
      // Handle form submission
    },
  },
}
</script>

<style scoped>
/* Add your styles here */
</style>
